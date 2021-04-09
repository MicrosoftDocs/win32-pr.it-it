---
description: Di seguito vengono fornite alcune istanze comuni di istruzioni condizionali. Per altre informazioni, vedere Sintassi dell'istruzione condizionale.
ms.assetid: 8b6bae7a-20ae-494c-bd96-66bd537c8630
title: Esempi di sintassi di istruzioni condizionali
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ca91a2b3e89160fad19ad5d9b1c6a3d33929e5d8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103967190"
---
# <a name="examples-of-conditional-statement-syntax"></a>Esempi di sintassi di istruzioni condizionali

Di seguito vengono fornite alcune istanze comuni di istruzioni condizionali. Per altre informazioni, vedere [sintassi dell'istruzione condizionale](conditional-statement-syntax.md).

## <a name="run-action-on-removal"></a>Eseguire un'azione durante la rimozione.

Per informazioni, vedere [condizionare le azioni da eseguire durante la rimozione](conditioning-actions-to-run-during-removal.md).

## <a name="run-action-only-if-the-product-has-not-been-installed"></a>Eseguire l'azione solo se il prodotto non è stato installato.

``` syntax
NOT Installed
```

## <a name="run-action-only-if-the-product-will-be-installed-local-do-not-run-action-on-a-reinstallation"></a>Eseguire l'azione solo se il prodotto verrà installato localmente. Non eseguire un'azione su una reinstallazione.

``` syntax
(&FeatureName=3) AND NOT(!FeatureName=3)
```

Il termine "&FeatureName = 3" indica che l'azione prevede l'installazione della funzionalità locale. Il termine "NOT (! FeatureName = 3) "indica che la funzionalità non è installata localmente.

## <a name="run-action-only-if-the-feature-will-be-uninstalled"></a>Eseguire l'azione solo se la funzionalità verrà disinstallata.

``` syntax
(&FeatureName=2) AND (!FeatureName=3)
```

Questa condizione controlla solo la presenza di una transizione della funzionalità da uno stato installato locale a quello assente.

## <a name="run-action-only-if-the-component-was-installed-local-but-is-transitioning-out-of-state"></a>Eseguire l'azione solo se il componente è stato installato localmente, ma è in fase di transizione allo stato.

``` syntax
(?ComponentName=3) AND ($ComponentName=2 OR $ComponentName=4)
```

Il termine "? ComponetName = 3 "indica che il componente è installato localmente. Il termine "$ComponentName = 2" indica che lo stato dell'azione nel componente è assente. Il termine "$ComponentName = 4" indica che lo stato dell'azione nel componente viene eseguito dall'origine. Si noti che lo stato di un'azione di annuncio non è valido per un componente.

## <a name="run-action-only-on-the-reinstallation-of-a-component"></a>Eseguire un'azione solo sulla reinstallazione di un componente.

``` syntax
?ComponentName=$ComponentName
```

## <a name="run-action-only-when-a-particular-patch-is-applied"></a>Eseguire un'azione solo quando viene applicata una particolare patch.

``` syntax
PATCH AND PATCH >< MEDIASRCPROPNAME
```

Per ulteriori informazioni, vedere la sezione Osservazioni nella pagina delle proprietà della [**patch**](patch.md) .

 

 



