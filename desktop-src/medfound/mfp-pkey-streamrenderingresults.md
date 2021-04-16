---
description: Specifica i flussi connessi correttamente a un sink multimediale.
ms.assetid: b5e45bfc-d91d-41b8-aaa4-72b3a23d869e
title: Proprietà MFP_PKEY_StreamRenderingResults (mfplay. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6acf04f751e8611f3add3a62fc7b4406d757999e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104343926"
---
# <a name="mfp_pkey_streamrenderingresults-property"></a>\_Proprietà StreamRenderingResults pkey di MFP \_

> [!IMPORTANT]
> Deprecato. Questa API può essere rimossa dalle versioni successive di Windows. Le applicazioni devono usare la [sessione multimediale](media-session.md) per la riproduzione.

 

Specifica i flussi connessi correttamente a un sink multimediale.



Tipo di dati

Tipo PROPVARIANT (VT)

membro PROPVARIANT

Matrice di valori **DWORD** (**Caul**)

VT \_ vettore \| VT \_ UI4

**CAUL**



## <a name="remarks"></a>Commenti

Questa proprietà può essere inviata con il **\_ tipo di evento MFP MEDIAITEM evento \_ \_ \_ set** .

Il valore della proprietà è una matrice di **HRESULT** s. Le voci della matrice corrispondono ai flussi sull'elemento multimediale corrente. Ogni voce della matrice indica se il flusso corrispondente è stato connesso a un sink multimediale, come indicato di seguito:

-   Se il flusso è connesso a un sink multimediale, il valore è **\_ OK**.
-   Se il flusso non è selezionato, il valore è **\_ false**.
-   Se si è verificato un errore durante il tentativo di connessione del flusso, il valore è un codice di errore.

Se almeno un flusso è stato connesso correttamente, è possibile eseguire la riproduzione. Ad esempio, l'utente potrebbe avere il codec necessario per riprodurre il flusso audio ma non per riprodurre il flusso video.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows 7\]<br/>                                          |
| Server minimo supportato<br/> | Solo app desktop Windows Server 2008 R2 \[\]<br/>                             |
| Intestazione<br/>                   | <dl> <dt>Mfplay. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Proprietà Media Foundation](media-foundation-properties.md)
</dt> <dt>

[**\_ \_ evento set MEDIAITEM \_ MFP**](/windows/desktop/api/mfplay/ns-mfplay-mfp_mediaitem_set_event)
</dt> </dl>

 

 




