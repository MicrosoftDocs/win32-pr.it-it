---
title: Raggruppamenti predefiniti (Ctffunc.h)
description: I valori seguenti identificano i raggruppamenti implementati da Framework servizi di testo.
ms.assetid: 65177979-ff91-4f62-8ba5-3c426b221b6c
keywords:
- Raggruppamenti predefiniti Framework servizi di testo
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
ms.openlocfilehash: 6c7c59312f7511c093f0d4c51bbdb9491f44b17cd16475e2b4261eaa676836e5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118876183"
---
# <a name="predefined-compartments"></a>Raggruppamenti predefiniti

I valori seguenti identificano i raggruppamenti implementati da Framework servizi di testo.

Gli identificatori di raggruppamento seguenti sono definiti in Ctffunc.idl e Ctffunc.h.



| Flag                                     | valore  | Descrizione                                                                                                                                                                                                                                                                               |
|------------------------------------------|--------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| GUID \_ COMPARTMENT \_ SAPI \_ AUDIO           | VT \_ I4 | Valore **DWORD** pari a zero se l'audio Speech API (SAPI) è disattivato o diverso da zero se l'audio SAPI è on. Questo raggruppamento è specifico di un oggetto di gestione thread.                                                                                                                               |
| GUID \_ COMPARTMENT \_ SPEECH \_ CFGMENU       | VT \_ I4 | Valore **DWORD** pari a zero se il menu di configurazione del riconoscimento vocale non è disponibile o diverso da zero se il menu di configurazione del riconoscimento vocale è disponibile. Questo raggruppamento è specifico di un oggetto di gestione thread.                                                                                               |
| GUID \_ COMPARTMENT \_ SPEECH \_ DICTATIONSTAT | VT \_ I4 | Valore **DWORD** che contiene zero o una combinazione di uno o più valori [**TF \_ DICTATION \_ ENABLED,**](speech-recognition-constants.md) **TF \_ COMMANDING \_ ENABLED,** **TF \_ DICTATION \_ ON** o **TF \_ COMMANDING \_ ON.** Questo raggruppamento è specifico di un oggetto di gestione thread. |
| STATO \_ \_ DELL'INTERFACCIA UTENTE DI RICONOSCIMENTO \_ VOCALE DEL RAGGRUPPAMENTO \_ GUID    | VT \_ I4 | Valore **DWORD** che contiene zero o una combinazione di uno o più valori [**TF \_ SHOW \_ BALLOON**](speech-recognition-constants.md) o **TF DISABLE \_ \_ BALLOON.** Si tratta di un raggruppamento globale.                                                                                   |



 

Gli identificatori di raggruppamento seguenti sono definiti in MSCTF. IDL e MSCTF.H.



| Flag                                                    | valore  | Descrizione                                                                                                                                                                                                                                                   |
|---------------------------------------------------------|--------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| GUID \_ COMPARTMENT \_ EMPTYCONTEXT                         | VT \_ I4 | Valore **DWORD diverso** da zero se il contesto è vuoto o zero in caso contrario. Questo raggruppamento è specifico di un oggetto contesto.                                                                                                                                      |
| GUID \_ COMPARTMENT \_ HANDWRITING \_ OPENCLOSE               | VT \_ I4 | Valore **DWORD diverso** da zero se il riconoscimento della grafia è aperto o zero se il riconoscimento della grafia è chiuso. Questo raggruppamento è specifico di un oggetto di gestione thread.                                                                                 |
| TASTIERA \_ \_ RAGGRUPPAMENTO GUID \_ DISABILITATA                   | VT \_ I4 | Valore **DWORD diverso** da zero se la tastiera è disabilitata o zero in caso contrario. Questo raggruppamento è specifico di un oggetto contesto.                                                                                                                                  |
| \_CONVERSIONE \_ \_ INPUTMODE DELLA TASTIERA DEL RAGGRUPPAMENTO \_ GUID      | VT \_ I4 | Valore **DWORD** della combinazione appropriata di flag [**TF \_ CONVERSIONMODE. \_**](flags-for-conversion-mode.md) Questo raggruppamento è specifico di un oggetto di gestione thread.                                                                                      |
| FRASE \_ \_ \_ INPUTMODE DELLA TASTIERA RAGGRUPPAMENTO \_ GUID        | VT \_ I4 | Valore **DWORD** di [**TF \_ SENTENCEMODE \_**](flags-for-conversion-mode.md). Questo raggruppamento è specifico di un oggetto di gestione thread.                                                                                                                        |
| TASTIERA \_ DEL \_ RAGGRUPPAMENTO GUID \_ OPENCLOSE                  | VT \_ I4 | Valore **DWORD** diverso da zero se la tastiera è aperta o zero se la tastiera è chiusa. Questo raggruppamento è specifico di un oggetto di gestione thread.                                                                                                               |
| \_ \_ PERSISTMENUENABLED RAGGRUPPAMENTO GUID                   | VT \_ I4 | Valore **DWORD diverso** da zero per consentire al servizio di riconoscimento vocale di abilitare la voce di **menu** Salva dati voce oppure zero per disabilitarla. Questo raggruppamento è specifico di un oggetto di gestione documenti.                                                                   |
| RICONOSCIMENTO \_ VOCALE \_ RAGGRUPPAMENTO GUID \_ DISABILITATO                     | VT \_ I4 | Valore **DWORD** che contiene zero o una combinazione di uno o più valori [**TF \_ DISABLE \_ SPEECH,**](speech-recognition-constants.md) **TF DISABLE \_ \_ DICTATION** o **TF DISABLE \_ \_ COMMANDING.** Questo raggruppamento è specifico di un oggetto di gestione thread. |
| GUID \_ COMPARTMENT \_ SPEECH \_ OPENCLOSE                    | VT \_ I4 | Valore **DWORD diverso** da zero se l'input vocale è attivo o zero se l'input vocale è inattivo. Si tratta di un raggruppamento globale.                                                                                                                                      |
| SUGGERIMENTO \_ \_ RAGGRUPPAMENTO GUIDUISTATUS                          | VT \_ I4 | Attualmente non utilizzato.                                                                                                                                                                                                                                           |
| GUID \_ COMPARTMENT \_ TRANSITORYEXTENSION                  | VT \_ I4 | Valore **DWORD** [**TF \_ TRANSITORYEXTENSION \_ NONE,**](values-for-guid-compartment-transitoryextension.md) **TF \_ TRANSITORYEXTENSION \_ FLOATING** o **TF \_ TRANSITORYEXTENSION \_ ATSELECTION**. Questo raggruppamento è specifico di un oggetto di gestione documenti.  |
| GUID \_ COMPARTMENT \_ TRANSITORYEXTENSION \_ DOCUMENTMANAGER | VT \_ I4 | Valore IUnknown per [**l'interfaccia ITfDocumentMgr**](/windows/desktop/api/Msctf/nn-msctf-itfdocumentmgr) che fa riferimento al documento transitorio di questo gestore di documenti. Questo raggruppamento è specifico di un oggetto di gestione documenti.                                                         |
| GUID \_ COMPARTMENT \_ TRANSITORYEXTENSION \_ PARENT          | VT \_ I4 | Valore IUnknown per [**l'interfaccia ITfDocumentMgr**](/windows/desktop/api/Msctf/nn-msctf-itfdocumentmgr) che fa riferimento al gestore documenti padre di questo documento transitorio. Questo raggruppamento è specifico di un oggetto di gestione documenti.                                                  |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                                                                                               |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                                                                                     |
| Componente ridistribuibile<br/>          | TSF 1.0 in Windows 2000 Professional<br/>                                                                                                          |
| Intestazione<br/>                   | <dl> <dt>Ctffunc.h; </dt> <dt>Mstctf.h</dt> </dl>     |
| Idl<br/>                      | <dl> <dt>Ctffunc.idl; </dt> <dt>Mstctf.idl</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Costanti di riconoscimento vocale**](speech-recognition-constants.md)
</dt> </dl>

 

 





