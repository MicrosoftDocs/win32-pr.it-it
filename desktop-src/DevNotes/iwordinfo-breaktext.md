---
description: Analizza il testo per identificare le parole e fornisce i risultati all'oggetto WordSink.
ms.assetid: 42bfc961-c095-4380-9b55-b58a0d9f2c00
title: Metodo IWordInfo::BreakText
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWordInfo.BreakText
api_type:
- COM
api_location:
- Msir3jp.dll
ms.openlocfilehash: 4cb4e4b27b52a4fb22a65f382a20c51a43ca5c77feb14828a7ea252e75c3b0f1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119749741"
---
# <a name="iwordinfobreaktext-method"></a>Metodo IWordInfo::BreakText

\[Questo metodo è obsoleto e non è supportato in Windows Vista.\]

Analizza il testo per identificare le parole e fornisce i risultati [all'oggetto WordSink.](/previous-versions//ms691570(v=vs.85))

## <a name="syntax"></a>Sintassi


```C++
HRESULT BreakText(
  [in] TEXT_SOURCE *pTextSource,
  [in] IWordSink   *pWordSink,
  [in] DWORD       fBreakMode
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pTextSource* \[ Pollici\]
</dt> <dd>

Puntatore a una [struttura TEXT \_ SOURCE](/previous-versions//ms690919(v=vs.85)) che contiene il testo Unicode.

</dd> <dt>

*pWordSink* \[ Pollici\]
</dt> <dd>

Puntatore [all'oggetto WordSink](/previous-versions//ms691570(v=vs.85)) che riceve e gestisce le parole generate da questo metodo. Se questo parametro è **NULL,** il metodo non suddivide la stringa in parole.

</dd> <dt>

*fBreakMode* \[ Pollici\]
</dt> <dd>

Modalità di interruzione. Questo parametro può avere uno dei valori seguenti.



| Valore                                                                                                                                                                                                                                                                                   | Significato                                                                                                     |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------|
| <span id="IWORDINFO_BREAKTEXTMODE_DICTFORM"></span><span id="iwordinfo_breaktextmode_dictform"></span><dl> <dt>**IWORDINFO \_ BREAKTEXTMODE \_ DICTFORM**</dt> <dt>0x00000002</dt> </dl> | Word interrompe la stringa di testo e passa la forma del dizionario delle parole **all'oggetto WordSink.**<br/> |
| <span id="IWORDINFO_BREAKTEXTMODE_SMARTSEL"></span><span id="iwordinfo_breaktextmode_smartsel"></span><dl> <dt>**IWORDINFO \_ BREAKTEXTMODE \_ SMARTSEL**</dt> <dt>0x00000001</dt> </dl> | Word interrompe la stringa di testo e passa le parole **all'oggetto WordSink.**<br/>                        |



 

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo restituisce uno dei valori seguenti.



| Codice restituito                                                                            | Descrizione                                                                                             |
|----------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>   | Operazione completata. Non è disponibile altro testo per riempire nuovamente il buffer *pTextSource.*<br/> |
| <dl> <dt>**E \_ FAIL**</dt> </dl> | Il *parametro pTextSource* è **NULL.**<br/>                                                     |



 

## <a name="remarks"></a>Commenti

Usare il **membro pfnFillTextBuffer** della struttura **TEXT \_ SOURCE** per riempire il testo di origine. Questo metodo deve gestire tutti i valori restituiti dalla funzione di callback **pfnFillTextBuffer.** Se si verifica un errore, terminare l'elaborazione del testo nel buffer prima di gestirlo.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop XP\]<br/>                                            |
| Server minimo supportato<br/> | Windows Solo app desktop server 2003 \[\]<br/>                                   |
| Fine del supporto client<br/>    | Windows XP<br/>                                                                  |
| Fine del supporto server<br/>    | Windows Server 2003<br/>                                                         |
| DLL<br/>                      | <dl> <dt>Msir3jp.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IWordInfo**](iwordinfo.md)
</dt> <dt>

[ORIGINE \_ TESTO](/previous-versions//ms690919(v=vs.85))
</dt> <dt>

[**WordInfo**](wordinfo-coclass.md)
</dt> <dt>

[WordSink](/previous-versions//ms691570(v=vs.85))
</dt> </dl>

 

 
