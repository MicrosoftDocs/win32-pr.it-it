---
title: Pointer-Attribute ereditarietà dei tipi
description: In base alla specifica DCE, ogni file IDL deve definire attributi per i relativi puntatori.
ms.assetid: ab8821ce-d52a-42bf-aa5e-582bb24adf93
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bcf0b365cecf2880fa2746536c3f1d80505f5d7534b95017f8abb18ceecd9d09
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120019261"
---
# <a name="pointer-attribute-type-inheritance"></a>Pointer-Attribute ereditarietà dei tipi

In base alla specifica DCE, ogni file IDL deve definire attributi per i relativi puntatori. Se un attributo esplicito non viene assegnato a un puntatore, il puntatore usa il valore specificato dalla parola chiave \[ [ \_ predefinita del](/windows/desktop/Midl/pointer-default) \] puntatore. Alcune implementazioni DCE non consentono puntatori senza attributi. Se un puntatore non ha un attributo esplicito, il file IDL deve avere **\[ \_ \]** una specifica predefinita del puntatore in modo che sia possibile impostare l'attributo del puntatore.

In modalità predefinita (estensioni Microsoft) è possibile specificare l'attributo di un puntatore nel file IDL che importa il file IDL di definizione. I puntatori definiti in un file IDL possono ereditare gli attributi specificati in altri file IDL. Inoltre, in modalità predefinita, i file IDL possono includere puntatori senza attributi. Se né la base né i file IDL **\[ \_ \]** importati specificano un attributo puntatore o un valore predefinito del puntatore, i puntatori senza attributi vengono interpretati come puntatori univoci.

Il compilatore MIDL assegna gli attributi del puntatore ai puntatori usando le regole di priorità seguenti (1 è il valore più alto).



| Priorità | Descrizione                                                                                                                |
|----------|----------------------------------------------------------------------------------------------------------------------------|
| 1        | Gli attributi espliciti del puntatore vengono applicati al puntatore in corrispondenza della definizione o del sito di utilizzo.                                      |
| 2        | Il valore predefinito è **\[ \_ l'attributo \]** predefinito del puntatore nel file IDL che definisce il tipo.                               |
| 3        | Il valore predefinito è **\[ \_ l'attributo \]** predefinito del puntatore nel file IDL che importa il tipo.                               |
| 4        | Il valore predefinito \[ [è ptr](/windows/desktop/Midl/ptr) \] in modalità di compatibilità DCE o \[ [univoco](/windows/desktop/Midl/unique) \] in modalità estensioni Microsoft. |



 

 

 