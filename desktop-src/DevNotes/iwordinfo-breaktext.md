---
description: Analizza il testo per identificare le parole e fornisce i risultati all'oggetto WordSink.
ms.assetid: 42bfc961-c095-4380-9b55-b58a0d9f2c00
title: 'Metodo IWordInfo:: BreakText'
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
ms.openlocfilehash: f6f71e92137490d56c93d9443506c2d7ffa2688a
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104049103"
---
# <a name="iwordinfobreaktext-method"></a>Metodo IWordInfo:: BreakText

\[Questo metodo è obsoleto e non è supportato in Windows Vista.\]

Analizza il testo per identificare le parole e fornisce i risultati all'oggetto [WordSink](/previous-versions//ms691570(v=vs.85)) .

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

*pTextSource* \[ in\]
</dt> <dd>

Puntatore a una struttura [di \_ origine di testo](/previous-versions//ms690919(v=vs.85)) che contiene il testo Unicode.

</dd> <dt>

*pWordSink* \[ in\]
</dt> <dd>

Puntatore all'oggetto [WordSink](/previous-versions//ms691570(v=vs.85)) che riceve e gestisce le parole generate da questo metodo. Se questo parametro è **null**, il metodo non suddivide la stringa in parole.

</dd> <dt>

*fBreakMode* \[ in\]
</dt> <dd>

Modalità di interruzioni. Questo parametro può avere uno dei valori seguenti.



| Valore                                                                                                                                                                                                                                                                                   | Significato                                                                                                     |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------|
| <span id="IWORDINFO_BREAKTEXTMODE_DICTFORM"></span><span id="iwordinfo_breaktextmode_dictform"></span><dl> <dt>**IWORDINFO \_ BREAKTEXTMODE \_ DICTFORM**</dt> <dt>0x00000002</dt> </dl> | Word interrompe la stringa di testo e passa il formato del dizionario delle parole all'oggetto **WordSink** .<br/> |
| <span id="IWORDINFO_BREAKTEXTMODE_SMARTSEL"></span><span id="iwordinfo_breaktextmode_smartsel"></span><dl> <dt>**IWORDINFO \_ BREAKTEXTMODE \_ SMARTSEL**</dt> <dt>0x00000001</dt> </dl> | Word interrompe la stringa di testo e passa le parole all'oggetto **WordSink** .<br/>                        |



 

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo restituisce uno dei valori seguenti.



| Codice restituito                                                                            | Descrizione                                                                                             |
|----------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>   | Operazione completata. Non è disponibile altro testo per riempire il buffer *pTextSource* .<br/> |
| <dl> <dt>**E \_ non riescono**</dt> </dl> | Il parametro *pTextSource* è **null**.<br/>                                                     |



 

## <a name="remarks"></a>Commenti

Usare il membro **pfnFillTextBuffer** della struttura **di \_ origine del testo** per riempire il testo di origine. Questo metodo deve gestire tutti i valori restituiti dalla funzione di callback **pfnFillTextBuffer** . Se si verifica un errore, completare l'elaborazione del testo nel buffer prima di gestire l'errore.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop Windows XP\]<br/>                                            |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                   |
| Fine del supporto client<br/>    | Windows XP<br/>                                                                  |
| Fine del supporto server<br/>    | Windows Server 2003<br/>                                                         |
| DLL<br/>                      | <dl> <dt>Msir3jp.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IWordInfo**](iwordinfo.md)
</dt> <dt>

[\_origine testo](/previous-versions//ms690919(v=vs.85))
</dt> <dt>

[**WordInfo**](wordinfo-coclass.md)
</dt> <dt>

[WordSink](/previous-versions//ms691570(v=vs.85))
</dt> </dl>

 

 
