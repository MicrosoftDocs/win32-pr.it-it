---
description: Il metodo ActivateButton attiva il pulsante di menu selezionato.
ms.assetid: 1da486a0-dadc-4c92-b3d3-83aeace01e39
title: Metodo ActivateButton
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c8a463a3aad1ee0dcabc0e5daaa4a4969efa37aa
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "106304210"
---
# <a name="activatebutton-method"></a>Metodo ActivateButton

> [!Note]  
> Questo componente è disponibile per l'uso nei sistemi operativi Microsoft Windows 2000, Windows XP e Windows Server 2003. È possibile che in versioni successive sia stata modificata o non sia più disponibile.

 

Il metodo ActivateButton attiva il pulsante di menu selezionato.

``` syntax
        MSWebDVD.ActivateButton()
```

## <a name="return-value"></a>Valore restituito

Nessun valore restituito.

## <a name="remarks"></a>Commenti

Utilizzare questo metodo quando si implementa la gestione personalizzata del mouse dopo l'impostazione di [**DisableAutoMouseProcessing**](disableautomouseprocessing-property.md) su **true**.

Usare questo metodo per attivare un pulsante che è stato selezionato tramite il metodo [**SelectLeftButton**](selectleftbutton-method.md), [**SelectLowerButton**](selectlowerbutton-method.md), [**SelectUpperButton**](selectupperbutton-method.md)o [**SelectRightButton**](selectrightbutton-method.md) .

 

 



