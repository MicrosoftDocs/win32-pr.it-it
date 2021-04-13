---
title: Ereditarietà del tipo di Pointer-Attribute
description: In base alla specifica DCE, ogni file IDL deve definire gli attributi per i relativi puntatori.
ms.assetid: ab8821ce-d52a-42bf-aa5e-582bb24adf93
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 182b7d46774484a9520424fd82bcff2d7103aa3c
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104399541"
---
# <a name="pointer-attribute-type-inheritance"></a>Ereditarietà del tipo di Pointer-Attribute

In base alla specifica DCE, ogni file IDL deve definire gli attributi per i relativi puntatori. Se un attributo esplicito non è assegnato a un puntatore, il puntatore utilizzerà il valore specificato dalla \[ parola chiave [ \_ default del puntatore](/windows/desktop/Midl/pointer-default) \] . Alcune implementazioni di DCE non consentono puntatori senza attributi. Se un puntatore non ha un attributo esplicito, il file IDL deve avere una specifica **\[ \_ predefinita \] del puntatore** , in modo che sia possibile impostare l'attributo del puntatore.

In modalità predefinita (Microsoft-Extensions) è possibile specificare l'attributo di un puntatore nel file IDL che importa il file IDL di definizione. I puntatori definiti in un file IDL possono ereditare gli attributi specificati in altri file IDL. Inoltre, in modalità predefinita, i file IDL possono includere puntatori senza attributi. Se né la base né i file IDL importati specificano un attributo puntatore o un **\[ puntatore \_ predefinito \]**, i puntatori senza attributi vengono interpretati come puntatori univoci.

Il compilatore MIDL assegna gli attributi del puntatore ai puntatori usando le seguenti regole di priorità (1 è il più alto).



| Priorità | Descrizione                                                                                                                |
|----------|----------------------------------------------------------------------------------------------------------------------------|
| 1        | Gli attributi di puntatore espliciti vengono applicati al puntatore nella definizione o usano il sito.                                      |
| 2        | Il valore predefinito è l'attributo **\[ \_ predefinito \] del puntatore** nel file IDL che definisce il tipo.                               |
| 3        | Il valore predefinito è l'attributo **\[ \_ predefinito \] del puntatore** nel file IDL che importa il tipo.                               |
| 4        | Il valore predefinito è \[ [ptr](/windows/desktop/Midl/ptr) \] in modalità di compatibilità DCE o \[ [univoco](/windows/desktop/Midl/unique) \] in modalità estensioni Microsoft. |



 

 

 