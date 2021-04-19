---
description: Inserisce una parola alternativa e la relativa posizione nell'oggetto IWordSink.
ms.assetid: 5C8A9B30-F9B5-42E9-ADAC-A11230F0C2FA
title: Metodo IWordSink::P utAltWord (search. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWordSink.PutAltWord
api_type:
- COM
api_location:
- search.h
ms.openlocfilehash: 21fd9eb9ac5a1bf0f52d6574595dc495432d7ec9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106306096"
---
# <a name="iwordsinkputaltword-method"></a>IWordSink::P metodo utAltWord

Inserisce una parola alternativa e la relativa posizione nell'oggetto [**IWordSink**](iwordsink.md) .

## <a name="syntax"></a>Sintassi


```C++
HRESULT PutAltWord(
  [in]       ULONG cwc,
  [in] const WCHAR *pwcInBuf,
  [in]       ULONG cwcSrcLen,
  [in]       ULONG cwcSrcPos
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*CWC* \[ in\]
</dt> <dd>

Numero di caratteri in *pwcInBuf*.

</dd> <dt>

*pwcInBuf* \[ in\]
</dt> <dd>

Puntatore a un buffer che contiene una forma alternativa di una parola dal testo di origine. Questo parametro non viene modificato da **PutAltWord**. È possibile passare il parametro *pTextSource* da [**IWordBreaker:: BreakText**](/windows/win32/api/indexsrv/nf-indexsrv-iwordbreaker-breaktext) , in base alle esigenze.

</dd> <dt>

*cwcSrcLen* \[ in\]
</dt> <dd>

Il numero di caratteri nel buffer di testo di origine (indicato dal parametro *pTextSource* in [**IWordBreaker:: BreakText**](/windows/win32/api/indexsrv/nf-indexsrv-iwordbreaker-breaktext)) che corrispondono alla parola contenuta in *pwcInBuf*.

</dd> <dt>

*cwcSrcPos* \[ in\]
</dt> <dd>

Posizione iniziale della parola in *pwcInBuf* nel buffer del testo di origine (indicata dal parametro *pTextSource* per [**IWordBreaker:: BreakText**](/windows/win32/api/indexsrv/nf-indexsrv-iwordbreaker-breaktext)).

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo può restituire uno di questi valori.



| Codice restituito                                                                                              | Descrizione                                                                                                                                               |
|----------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>                     | L'operazione è stata completata correttamente. Indica inoltre che non resta altro testo da elaborare.<br/>                                            |
| <dl> <dt>**Lingua \_ di \_ \_ parola grande**</dt> </dl> | Il valore di *CWC* è maggiore del valore di *UlMaxTokenSize* specificato in [**IWordBreaker:: init**](/windows/win32/api/indexsrv/nf-indexsrv-iwordbreaker-init). <br/> |



 

## <a name="remarks"></a>Commenti

**PutAltWord** inserisce una forma alternativa di una parola in [**IWordSink**](iwordsink.md). La parola viene posizionata nella stessa posizione della parola originale nell'origine testo (*pTextSource* in [**IWordBreaker:: BreakText**](/windows/win32/api/indexsrv/nf-indexsrv-iwordbreaker-breaktext)). Per impostazione predefinita, **PutAltWord** termina le parole con un tipo di interruzione **WORDREP \_ break \_ EOW** dal tipo enumerato [**WORDREP \_ \_ tipo di interruzione**](/previous-versions/windows/desktop/legacy/ff819130(v=vs.85)) .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                          |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                |
| Intestazione<br/>                   | <dl> <dt>Search. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IWordSink**](iwordsink.md)
</dt> </dl>

 

 
