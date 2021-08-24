---
description: La proprietà DisableAutoMouseProcessing abilita o disabilita la funzionalità di elaborazione del mouse dell'oggetto MSWebDVD.
ms.assetid: d438deb8-3c6d-49c1-923b-d4c57e236fc9
title: Proprietà DisableAutoMouseProcessing
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c9728f968e1ce562bc8cc643b5c27b8ac2ace3db1b2d39c45a8ae1fa78b44971
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119749151"
---
# <a name="disableautomouseprocessing-property"></a>Proprietà DisableAutoMouseProcessing

> [!Note]  
> Questo componente è disponibile per l'uso nei sistemi operativi Microsoft Windows 2000, Windows XP e Windows Server 2003. È possibile che in versioni successive sia stata modificata o non sia più disponibile.

 

La proprietà abilita o disabilita la funzionalità di elaborazione del `DisableAutoMouseProcessing` mouse dell'oggetto **MSWebDVD.**

``` syntax
[ bMouseProcessing = ] MSWebDVD.DisableAutoMouseProcessing
```

## <a name="return-value"></a>Valore restituito

Restituisce un valore booleano che indica se disabilitare l'elaborazione predefinita del mouse.

## <a name="remarks"></a>Commenti

Questa proprietà è di lettura/scrittura con il valore predefinito false. **L'oggetto MSWebDVD** gestisce automaticamente le azioni del mouse per i menu dvd su schermo per impostazione predefinita. gli utenti possono evidenziare e attivare i pulsanti di menu senza programmazione speciale da parte dell'applicazione. Un'applicazione può disattivare questa funzionalità di gestione del mouse predefinita impostando questa proprietà su **true.** Quando l'elaborazione automatica del mouse è disattivata, un'applicazione deve usare i vari metodi e proprietà correlati ai pulsanti per gestire gli spostamenti del mouse e i clic del mouse nei menu sullo schermo. Inoltre, un'applicazione può usare i metodi correlati al pulsante per eseguire l'override della gestione automatica del mouse anche quando è `DisableAutoMouseProcessing` impostata su **false**.

 

 



