The Adversarial Robustness Toolbox had five types of defenses as of version 1.8:

· Detector. You can use the detector defense to detect adversarial samples. There are different detection methods implemented in ART — Activation Defense, for example, uses a victim model’s activations(biases and weights) to cluster samples into clean and adversarial groups. As of version 1.8, ART had detectors only for evasion and poisoning attacks.

· Transformer. Transformer defenses apply perturbations to the provided input to reveal adversarial samples. These defenses measure the effect that the perturbations had on the model output and flag outliers as poisoned samples(the ones reacting abruptly to the output of the model). As of version 1.8, ART had transformer defenses only for poisoning and evasion attacks.

· Trainer. The trainer is a training-based defense where the model is trained on a combination of clean and adversarial samples. You essentially teach the model to predict the correct label for both clean and adversarial input. As of version 1.8, ART had trainer defenses only for evasion attacks.

· Preprocessor. The preprocessor defense applies some form of preprocessing to adversarial input to smoothen perturbations. This makes the adversarial samples look more like clean samples, which can improve model performance. ART’s preprocessing defenses may work for a wide range of attacks.

· Postprocessor. The postprocessing defense applies some form of processing to model outputs to hide their meaning from attackers. This defense is typically used against model stealing. Postprocessed outputs obscure how the model makes decisions, which can prevent model theft.

With all that in mind, when designing any type of AI defense, you should decide for yourself what levels of false positives and false negatives are appropriate.