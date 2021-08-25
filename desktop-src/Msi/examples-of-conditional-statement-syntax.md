---
description: Di seguito sono riportate alcune istanze comuni delle istruzioni condizionali. Per altre informazioni, vedere Sintassi delle istruzioni condizionali.
ms.assetid: 8b6bae7a-20ae-494c-bd96-66bd537c8630
title: Esempi di sintassi delle istruzioni condizionali
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 88445e1e4b371669c43b47d1ca54e9fd677c5414985ade3908b95e00717de887
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119811031"
---
# <a name="examples-of-conditional-statement-syntax"></a>Esempi di sintassi delle istruzioni condizionali

Di seguito sono riportate alcune istanze comuni delle istruzioni condizionali. Per altre informazioni, vedere [Sintassi delle istruzioni condizionali.](conditional-statement-syntax.md)

## <a name="run-action-on-removal"></a>Eseguire l'azione in fase di rimozione.

Per informazioni, vedere [Conditioning Actions to Run During Removal](conditioning-actions-to-run-during-removal.md).

## <a name="run-action-only-if-the-product-has-not-been-installed"></a>Eseguire l'azione solo se il prodotto non è stato installato.

``` syntax
NOT Installed
```

## <a name="run-action-only-if-the-product-will-be-installed-local-do-not-run-action-on-a-reinstallation"></a>Eseguire l'azione solo se il prodotto verrà installato in locale. Non eseguire alcuna azione su una reinstallazione.

``` syntax
(&FeatureName=3) AND NOT(!FeatureName=3)
```

Il termine "&FeatureName=3" indica che l'azione è installare la funzionalità in locale. Il termine "NOT(! FeatureName=3)" indica che la funzionalità non è installata in locale.

## <a name="run-action-only-if-the-feature-will-be-uninstalled"></a>Eseguire l'azione solo se la funzionalità verrà disinstallata.

``` syntax
(&FeatureName=2) AND (!FeatureName=3)
```

Questa condizione verifica solo la presenza di una transizione della funzionalità da uno stato installato locale a uno stato assente.

## <a name="run-action-only-if-the-component-was-installed-local-but-is-transitioning-out-of-state"></a>Eseguire l'azione solo se il componente è stato installato in locale, ma sta per uscire dallo stato .

``` syntax
(?ComponentName=3) AND ($ComponentName=2 OR $ComponentName=4)
```

Il termine "? ComponetName=3" indica che il componente è installato in locale. Il termine "$ComponentName=2" indica che lo stato dell'azione nel componente è Absent. Il termine "$ComponentName=4" indica che lo stato dell'azione nel componente viene eseguito dall'origine. Si noti che lo stato dell'azione advertise non è valido per un componente.

## <a name="run-action-only-on-the-reinstallation-of-a-component"></a>Eseguire l'azione solo durante la reinstallazione di un componente.

``` syntax
?ComponentName=$ComponentName
```

## <a name="run-action-only-when-a-particular-patch-is-applied"></a>Eseguire l'azione solo quando viene applicata una particolare patch.

``` syntax
PATCH AND PATCH >< MEDIASRCPROPNAME
```

Per altre informazioni, vedere la sezione Osservazioni nella pagina [**delle proprietà**](patch.md) PATCH.

 

 



