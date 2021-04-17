---
description: Le costanti dei criteri di controllo delle prestazioni del processore indicano l'algoritmo di controllo delle prestazioni del processore applicato a uno schema di risparmio energia.
ms.assetid: 928ba485-f767-47df-8b57-7630c68068a7
title: Costanti dei criteri di controllo delle prestazioni del processore (WinNT. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9597750f37d9efda80d4bb2bfff7bc121982e7d8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104529107"
---
# <a name="processor-performance-control-policy-constants"></a>Costanti dei criteri di controllo delle prestazioni del processore

Le costanti dei criteri di controllo delle prestazioni del processore indicano l'algoritmo di controllo delle prestazioni del processore applicato a uno schema di risparmio energia.



| Costante/valore                                                                                                                                                                                                                             | Descrizione                                                                                                                                                                                                                                                                                                                                                                                                                                       |
|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="PO_THROTTLE_ADAPTIVE"></span><span id="po_throttle_adaptive"></span><dl> <dt>**Ordine di acquisto \_ LIMITAZIONE \_ Adaptive**</dt> <dt>3</dt> </dl> | Tenta di far corrispondere le prestazioni del processore alla richiesta corrente. Questo criterio utilizzerà gli Stati di frequenza e di tensione alta e bassa. Questo criterio diminuisce le prestazioni del processore fino alla tensione minima disponibile quando la richiesta non è sufficiente per giustificare una tensione superiore. Questo criterio attiverà la limitazione del clock del processore se lo stato C3 non viene utilizzato e in risposta a eventi termici.<br/> |
| <span id="PO_THROTTLE_CONSTANT"></span><span id="po_throttle_constant"></span><dl> <dt>**Ordine di acquisto \_ \_Costante di limitazione**</dt> <dt>1</dt> </dl> | Non consente al processore di utilizzare alcun stato di prestazioni a tensione elevata. Questo criterio non attiverà la limitazione del clock del processore, tranne che in risposta ad eventi termici.<br/>                                                                                                                                                                                                                                                                 |
| <span id="PO_THROTTLE_DEGRADE"></span><span id="po_throttle_degrade"></span><dl> <dt>**Ordine di acquisto \_ LIMITAZIONE \_**</dt> <dt>2</dt> </dl>    | Non consente al processore di utilizzare alcun stato di prestazioni a tensione elevata. Questo criterio attiverà la limitazione del clock del processore quando la batteria si trova al di sotto di una determinata soglia, se lo stato C3 non è in uso o in risposta a eventi termici.<br/>                                                                                                                                                                                    |
| <span id="PO_THROTTLE_NONE"></span><span id="po_throttle_none"></span><dl> <dt>**Ordine di acquisto \_ LIMITAZIONE \_ Nessuna**</dt> <dt>0</dt> </dl>             | Non viene applicato alcun controllo delle prestazioni del processore. Questo criterio esegue sempre il processore al massimo livello di prestazioni possibile. Questo criterio non attiverà la limitazione del clock del processore, tranne che in risposta ad eventi termici.<br/>                                                                                                                                                                                                            |



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop Windows XP\]<br/>                                                            |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                                   |
| Intestazione<br/>                   | <dl> <dt>WinNT. h (include Windows. h)</dt> </dl> |



 

 




