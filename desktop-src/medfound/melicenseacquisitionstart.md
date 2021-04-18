---
description: Generato dal motore dei criteri quando l'acquisizione della licenza sta per iniziare. L'acquisizione della licenza viene eseguita usando l'implementazione delle applicazioni dell'interfaccia IMFContentProtectionManager.
ms.assetid: c328743c-a69b-431e-8a05-0e140aad9b4d
title: Evento MELicenseAcquisitionStart (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 914d2580c95cf40986a844a994c1e284c5ad9e22
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106309634"
---
# <a name="melicenseacquisitionstart-event"></a>Evento MELicenseAcquisitionStart

Generato dal motore dei criteri quando l'acquisizione della licenza sta per iniziare. L'acquisizione della licenza viene eseguita usando l'implementazione dell'applicazione dell'interfaccia [**IMFContentProtectionManager**](/windows/desktop/api/mfidl/nn-mfidl-imfcontentprotectionmanager) .

## <a name="event-values"></a>Valori dell'evento

I valori possibili recuperati da [**IMFMediaEvent:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) includono i seguenti.



| VARTYPE              | Descrizione                           |
|----------------------|---------------------------------------|
| VT \_ vuoto<br/> | Nessun dato dell'evento.<br/> <br/> |



## <a name="remarks"></a>Commenti

Quando l'acquisizione della licenza viene completata, il motore dei criteri genera l'evento [MELicenseAcquisitionCompleted](melicenseacquisitioncompleted.md) .

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

 

 




