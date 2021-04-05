---
title: Raggruppamenti predefiniti (Ctffunc. h)
description: I valori seguenti identificano i raggruppamenti implementati da Text Services Framework.
ms.assetid: 65177979-ff91-4f62-8ba5-3c426b221b6c
keywords:
- Framework servizi di testo raggruppamenti predefiniti
topic_type:
- apiref
api_name:
- Predefined Compartments
api_location:
- Ctffunc.h
- Mstctf.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9fcc684c4aee55c3c2e1807458ee261ad55156e9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104120911"
---
# <a name="predefined-compartments"></a>Raggruppamenti predefiniti

I valori seguenti identificano i raggruppamenti implementati da Text Services Framework.

Gli identificatori di raggruppamento seguenti sono definiti in Ctffunc. idl e Ctffunc. h.



| Flag                                     | valore  | Descrizione                                                                                                                                                                                                                                                                               |
|------------------------------------------|--------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \_audio del raggruppamento GUID \_ \_           | VT \_ I4 | **Valore DWORD** che è zero se l'audio Speech API (SAPI) è disattivato o diverso da zero se l'audio SAPI è acceso. Questo raggruppamento è specifico di un oggetto gestore thread.                                                                                                                               |
| \_ \_ CFGMENU vocale raggruppamento \_ GUID       | VT \_ I4 | **Valore DWORD** che è zero se il menu di configurazione vocale non è disponibile o è diverso da zero se il menu di configurazione vocale è disponibile. Questo raggruppamento è specifico di un oggetto gestore thread.                                                                                               |
| \_ \_ DICTATIONSTAT vocale raggruppamento \_ GUID | VT \_ I4 | Valore **DWORD** che contiene zero o una combinazione di una o più della [**\_ Dettatura di TF \_ abilitata**](speech-recognition-constants.md), **del \_ comando tf \_ abilitato**, **della \_ Dettatura \_** di TF su o del **\_ comando tf \_ sui** valori. Questo raggruppamento è specifico di un oggetto gestore thread. |
| \_ \_ \_ stato dell'interfaccia utente del dialogo di raggruppamento GUID \_    | VT \_ I4 | Valore **DWORD** che contiene zero o una combinazione di uno o più dei valori del fumetto TF [**\_ Show \_**](speech-recognition-constants.md) o **tf \_ Disable \_** . Si tratta di un raggruppamento globale.                                                                                   |



 

Gli identificatori di raggruppamento seguenti sono definiti in MSCTF. IDL e MSCTF. H.



| Flag                                                    | valore  | Descrizione                                                                                                                                                                                                                                                   |
|---------------------------------------------------------|--------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \_EMPTYCONTEXT raggruppamento \_ GUID                         | VT \_ I4 | **Valore DWORD** che è diverso da zero se il contesto è vuoto o zero in caso contrario. Questo raggruppamento è specifico di un oggetto context.                                                                                                                                      |
| \_OPENCLOSE della \_ grafia del raggruppamento GUID \_               | VT \_ I4 | **Valore DWORD** che è diverso da zero se il riconoscimento della grafia è aperto o zero se il riconoscimento della grafia è chiuso. Questo raggruppamento è specifico di un oggetto gestore thread.                                                                                 |
| \_tastiera raggruppamento \_ GUID \_ disabilitata                   | VT \_ I4 | **Valore DWORD** che è diverso da zero se la tastiera è disabilitata o zero in caso contrario. Questo raggruppamento è specifico di un oggetto context.                                                                                                                                  |
| \_ \_ conversione INPUTMODE della tastiera del raggruppamento GUID \_ \_      | VT \_ I4 | Valore **DWORD** della combinazione appropriata di flag [**tf \_ CONVERSIONMODE \_**](flags-for-conversion-mode.md) . Questo raggruppamento è specifico di un oggetto gestore thread.                                                                                      |
| \_ \_ frase INPUTMODE della tastiera del raggruppamento GUID \_ \_        | VT \_ I4 | Valore **DWORD** di [**tf \_ SENTENCEMODE \_**](flags-for-conversion-mode.md). Questo raggruppamento è specifico di un oggetto gestore thread.                                                                                                                        |
| \_ \_ OPENCLOSE tastiera raggruppamento \_ GUID                  | VT \_ I4 | **Valore DWORD** che è diverso da zero se la tastiera è aperta o zero se la tastiera viene chiusa. Questo raggruppamento è specifico di un oggetto gestore thread.                                                                                                               |
| \_PERSISTMENUENABLED raggruppamento \_ GUID                   | VT \_ I4 | **DWORD** che è diverso da zero per fare in modo che il servizio di testo vocale consenta la voce di menu **Salva dati vocali** o zero per disabilitarlo. Questo raggruppamento è specifico di un oggetto di gestione documenti.                                                                   |
| \_voce raggruppamento \_ GUID \_ disabilitata                     | VT \_ I4 | **Valore DWORD** che contiene zero o una combinazione di uno o più dei comandi [**tf \_ Disable \_**](speech-recognition-constants.md), **tf \_ Disable \_ dettation** o **tf \_ Disable \_** . Questo raggruppamento è specifico di un oggetto gestore thread. |
| \_ \_ OPENCLOSE vocale raggruppamento \_ GUID                    | VT \_ I4 | **Valore DWORD** che è diverso da zero se l'input vocale è attivo o zero se l'input vocale è inattivo. Si tratta di un raggruppamento globale.                                                                                                                                      |
| \_TIPUISTATUS raggruppamento \_ GUID                          | VT \_ I4 | Attualmente non utilizzato.                                                                                                                                                                                                                                           |
| \_TRANSITORYEXTENSION raggruppamento \_ GUID                  | VT \_ I4 | Valore **DWORD** di [**tf \_ TRANSITORYEXTENSION \_ None**](values-for-guid-compartment-transitoryextension.md), **tf \_ TRANSITORYEXTENSION \_ Floating** o **tf \_ TRANSITORYEXTENSION \_ ATSELECTION**. Questo raggruppamento è specifico di un oggetto di gestione documenti.  |
| \_raggruppamento GUID \_ TRANSITORYEXTENSION \_ DOCUMENTMANAGER | VT \_ I4 | Valore IUnknown per l'interfaccia [**ITfDocumentMgr**](/windows/desktop/api/Msctf/nn-msctf-itfdocumentmgr) che fa riferimento al documento transitorio di questo gestore di documenti. Questo raggruppamento è specifico di un oggetto di gestione documenti.                                                         |
| \_ \_ elemento padre TRANSITORYEXTENSION raggruppamento GUID \_          | VT \_ I4 | Valore IUnknown per l'interfaccia [**ITfDocumentMgr**](/windows/desktop/api/Msctf/nn-msctf-itfdocumentmgr) che fa riferimento alla gestione documenti padre di questo documento temporaneo. Questo raggruppamento è specifico di un oggetto di gestione documenti.                                                  |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                                                                                               |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                                                                                     |
| Componente ridistribuibile<br/>          | TSF 1,0 su Windows 2000 Professional<br/>                                                                                                          |
| Intestazione<br/>                   | <dl> <dt>Ctffunc. h; </dt> <dt>Mstctf. h</dt> </dl>     |
| IDL<br/>                      | <dl> <dt>Ctffunc. idl; </dt> <dt>Mstctf. idl</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Costanti di riconoscimento vocale**](speech-recognition-constants.md)
</dt> </dl>

 

 





