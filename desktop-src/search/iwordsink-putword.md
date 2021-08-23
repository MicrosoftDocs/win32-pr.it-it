---
description: Inserisce una parola e la relativa posizione nell'oggetto IWordSink.
ms.assetid: 3D645BF6-895E-46E2-92A3-3E301CD228D8
title: Metodo IWordSink::P utWord (Search.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWordSink.PutWord
api_type:
- COM
api_location:
- search.h
ms.openlocfilehash: e860aafbef633e226933281aaaa0be5c6429387542e7c3ae2d65d3026fd7fe37
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119597601"
---
# <a name="iwordsinkputword-method"></a>Metodo IWordSink::P utWord

Inserisce una parola e la relativa posizione [**nell'oggetto IWordSink.**](iwordsink.md)

## <a name="syntax"></a>Sintassi


```C++
HRESULT PutWord(
  [in]       ULONG cwc,
  [in] const WCHAR *pwcInBuf,
  [in]       ULONG cwcSrcLen,
  [in]       ULONG cwcSrcPos
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*cwc* \[ Pollici\]
</dt> <dd>

Numero di caratteri in *pwcInBuf.*

</dd> <dt>

*pwcInBuf* \[ Pollici\]
</dt> <dd>

Puntatore a un buffer che contiene una forma alternativa di una parola dal testo di origine. Questo parametro non viene modificato da **PutWord.** È possibile passare il *parametro pTextSource* da [**IWordBreaker::BreakText in**](/windows/win32/api/indexsrv/nf-indexsrv-iwordbreaker-breaktext) base alle esigenze.

</dd> <dt>

*cwcSrcLen* \[ Pollici\]
</dt> <dd>

Numero di caratteri nel buffer di testo di origine (indicato dal parametro *pTextSource* a [**IWordBreaker::BreakText)**](/windows/win32/api/indexsrv/nf-indexsrv-iwordbreaker-breaktext)che corrispondono alla parola contenuta in *pwcInBuf.*

</dd> <dt>

*cwcSrcPos* \[ Pollici\]
</dt> <dd>

Posizione iniziale della parola in *pwcInBuf* nel buffer di testo di origine (indicata dal *parametro pTextSource* a [**IWordBreaker::BreakText).**](/windows/win32/api/indexsrv/nf-indexsrv-iwordbreaker-breaktext)

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo può restituire uno di questi valori.



| Codice restituito                                                                                              | Descrizione                                                                                                                                               |
|----------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                     | L'operazione è stata completata correttamente. Indica inoltre che non è disponibile altro testo per il riempimento del buffer.<br/>                                  |
| <dl> <dt>**LANGUAGE \_ S \_ LARGE \_ WORD**</dt> </dl> | Il valore *di cwc* è maggiore del valore di *ulMaxTokenSize* specificato in [**IWordBreaker::Init**](/windows/win32/api/indexsrv/nf-indexsrv-iwordbreaker-init). <br/> |



 

## <a name="remarks"></a>Commenti

È consigliabile che **il metodo IWordSink::P utWord** contenga sempre la parola originale trovata in *pTextSource.* Le forme alternative della parola vengono passate a WordSink usando [**IWordSink::P utAltWord**](iwordsink-putaltword.md). È anche consigliabile che le parole in *pwcInBuf* corrispondano il più possibile al testo di origine. Se possibile, ad esempio, mantenere le maiuscole e gli accenti.

Questa chiamata deve essere effettuata per ogni parola recuperata da *pTextSource,* ad eccezione di quelle per cui è stata effettuata la chiamata [**IWordSink::P utAltWord.**](iwordsink-putaltword.md) La parola termina con un carattere EOW quando viene salvata in WordSink.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                          |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                |
| Intestazione<br/>                   | <dl> <dt>Search.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IWordSink**](iwordsink.md)
</dt> </dl>

 

 
