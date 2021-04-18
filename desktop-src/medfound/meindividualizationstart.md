---
description: Generato dal motore dei criteri quando l'individualizzazione sta per iniziare. L'individualizzazione viene eseguita usando l'implementazione delle applicazioni dell'interfaccia IMFContentProtectionManager.
ms.assetid: a3ba98ee-4d2e-466d-be9a-c7e3b5f920a7
title: Evento MEIndividualizationStart (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dbb8d50bbc2081c4efa41d8b15cc3e41a14ab5eb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106309637"
---
# <a name="meindividualizationstart-event"></a>Evento MEIndividualizationStart

Generato dal motore dei criteri quando l'individualizzazione sta per iniziare. L'individualizzazione viene eseguita usando l'implementazione dell'applicazione dell'interfaccia [**IMFContentProtectionManager**](/windows/desktop/api/mfidl/nn-mfidl-imfcontentprotectionmanager) .

Un'applicazione personalizzata è una che ha ricevuto un aggiornamento ai componenti di Digital Rights Management (DRM) che li distingue da tutte le altre copie della stessa applicazione. I proprietari del contenuto possono richiedere che i file protetti vengano riprodotti solo in un'applicazione che è stata individualmente.

## <a name="event-values"></a>Valori dell'evento

I valori possibili recuperati da [**IMFMediaEvent:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) includono i seguenti.



| VARTYPE              | Descrizione                           |
|----------------------|---------------------------------------|
| VT \_ vuoto<br/> | Nessun dato dell'evento.<br/> <br/> |



## <a name="remarks"></a>Commenti

Quando l'acquisizione della licenza viene completata, il motore dei criteri genera l'evento [MEIndividualizationCompleted](meindividualizationcompleted.md) .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                                           |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/>                                                     |
| Intestazione<br/>                   | <dl> <dt>Mfobjects. h (include Mfidl. h)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Eventi Media Foundation](media-foundation-events.md)
</dt> </dl>

 

 




