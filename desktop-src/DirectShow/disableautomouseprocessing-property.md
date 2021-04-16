---
description: La proprietà DisableAutoMouseProcessing Abilita o Disabilita la funzionalità di elaborazione del mouse dell'oggetto MSWebDVD.
ms.assetid: d438deb8-3c6d-49c1-923b-d4c57e236fc9
title: Proprietà DisableAutoMouseProcessing
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b606392acd4030d68af9590555a40d571d70c581
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104480860"
---
# <a name="disableautomouseprocessing-property"></a>Proprietà DisableAutoMouseProcessing

> [!Note]  
> Questo componente è disponibile per l'uso nei sistemi operativi Microsoft Windows 2000, Windows XP e Windows Server 2003. È possibile che in versioni successive sia stata modificata o non sia più disponibile.

 

La `DisableAutoMouseProcessing` proprietà Abilita o Disabilita la funzionalità di elaborazione del mouse dell'oggetto **mswebdvd** .

``` syntax
[ bMouseProcessing = ] MSWebDVD.DisableAutoMouseProcessing
```

## <a name="return-value"></a>Valore restituito

Restituisce un valore booleano che indica se disabilitare l'elaborazione del mouse predefinita.

## <a name="remarks"></a>Commenti

Questa proprietà è di lettura/scrittura e il valore predefinito è false. Per impostazione predefinita, l'oggetto **mswebdvd** gestisce automaticamente le azioni del mouse per i menu su schermo DVD. Gli utenti possono evidenziare e attivare i pulsanti di menu senza programmazione speciale da parte dell'applicazione. Un'applicazione può disattivare questa funzionalità predefinita di gestione del mouse impostando questa proprietà su **true**. Quando l'elaborazione automatica del mouse è disattivata, un'applicazione deve utilizzare i vari metodi e proprietà correlati ai pulsanti per gestire i movimenti del mouse e i clic del mouse nei menu sullo schermo. Inoltre, un'applicazione può utilizzare i metodi correlati ai pulsanti per sostituire la gestione automatica del mouse anche quando `DisableAutoMouseProcessing` è impostato su **false**.

 

 



