---
title: Valori restituiti dell'archivio di testo (Textstor. h)
description: Quando un gestore di documenti elabora un archivio di testo, produce valori restituiti nell'intervallo compreso tra 0xHHHH0200 e 0xHHHH0300. Nella tabella seguente sono elencati i valori restituiti dell'archivio di testo in ordine alfabetico.
ms.assetid: 20b0a89f-ab52-466f-9669-c6c29ad12de0
topic_type:
- apiref
api_name:
- Text Store Return Values
api_location:
- Textstor.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: adc2e0141eea559371411455973f1fa4aa87f31e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104518400"
---
# <a name="text-store-return-values"></a>Valori restituiti dall'archivio di testo

Quando un gestore di documenti elabora un archivio di testo, produce valori restituiti compresi nell'intervallo da 0x *hhhh* 0200 a 0x *HHHH* 0300. Nella tabella seguente sono elencati i valori restituiti dell'archivio di testo in ordine alfabetico.



| Codice/valore restituito                                                                                                                                                                                                                          | Descrizione                                                                                                                                                                                                  |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TS_E_FORMAT"></span><span id="ts_e_format"></span><dl> <dt>**Servizi terminal \_ \_Formato E**</dt> <dt>0x8004020a</dt> </dl>                   | L'applicazione non supporta il tipo di dati contenuto nell'oggetto [**IDataObject**](/windows/desktop/api/objidl/nn-objidl-idataobject) da inserire con [**ITextStoreACP:: InsertEmbedded**](/windows/desktop/api/Textstor/nf-textstor-itextstoreacp-insertembedded).<br/> |
| <span id="TS_E_INVALIDPOINT"></span><span id="ts_e_invalidpoint"></span><dl> <dt>**Servizi terminal \_ E \_ INVALIDPOINT**</dt> <dt>0x80040207</dt> </dl> | Il parametro non si trova all'interno del rettangolo di delimitazione di un carattere.<br/>                                                                                                                                        |
| <span id="TS_E_INVALIDPOS"></span><span id="ts_e_invalidpos"></span><dl> <dt>**Servizi terminal \_ E \_ INVALIDPOS**</dt> <dt>0x80040200</dt> </dl>       | L'intervallo specificato si estende all'esterno del documento.<br/>                                                                                                                                                     |
| <span id="TS_E_NOINTERFACE"></span><span id="ts_e_nointerface"></span><dl> <dt>**Servizi terminal \_ E \_ nointerface**</dt> <dt>0x80040204</dt> </dl>    | L'oggetto non supporta l'interfaccia richiesta.<br/>                                                                                                                                                  |
| <span id="TS_E_NOLAYOUT"></span><span id="ts_e_nolayout"></span><dl> <dt>**Servizi terminal \_ E \_ nolayout**</dt> <dt>0x80040206</dt> </dl>             | L'applicazione non ha calcolato un layout di testo.<br/>                                                                                                                                                     |
| <span id="TS_E_NOLOCK"></span><span id="ts_e_nolock"></span><dl> <dt>**Servizi terminal \_ E \_ NOLOCK**</dt> <dt>0x80040201</dt> </dl>                   | L'applicazione non dispone di un blocco di sola lettura o di lettura/scrittura per il documento.<br/>                                                                                                                   |
| <span id="TS_E_NOOBJECT"></span><span id="ts_e_noobject"></span><dl> <dt>**Servizi terminal \_ E \_ noobject**</dt> <dt>0x80040202</dt> </dl>             | L'offset del contenuto incorporato non è posizionato prima di un \_ \_ carattere incorporato TF Char.<br/>                                                                                                                  |
| <span id="TS_E_NOSELECTION"></span><span id="ts_e_noselection"></span><dl> <dt>**Servizi terminal \_ E \_ NOselection**</dt> <dt>0x80040205</dt> </dl>    | Nessun documento selezionato.<br/>                                                                                                                                                                        |
| <span id="TS_E_NOSERVICE"></span><span id="ts_e_noservice"></span><dl> <dt>**Servizi terminal \_ No0x80040203 E \_ noservice**</dt> <dt></dt> </dl>          | Non è possibile restituire il contenuto in modo che corrisponda al GUID del servizio.<br/>                                                                                                                                             |
| <span id="TS_E_READONLY"></span><span id="ts_e_readonly"></span><dl> <dt>**Servizi terminal \_ 0x80040209 E \_ ReadOnly**</dt> <dt></dt> </dl>             | Documento di sola lettura. Impossibile modificare il contenuto.<br/>                                                                                                                                                     |
| <span id="TS_E_SYNCHRONOUS"></span><span id="ts_e_synchronous"></span><dl> <dt>**Servizi terminal \_ 0x00040300 \_ sincrono E**</dt> <dt></dt> </dl>    | Il documento non può essere bloccato in modo sincrono.<br/>                                                                                                                                                          |
| <span id="TS_S_ASYNC"></span><span id="ts_s_async"></span><dl> <dt>**Servizi terminal \_ \_Asincrono S**</dt> <dt>(0x1)</dt> </dl>                         | Il documento ha ricevuto un blocco asincrono.<br/>                                                                                                                                              |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                              |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                    |
| Componente ridistribuibile<br/>          | TSF 1,0 su Windows 2000 Professional<br/>                                         |
| Intestazione<br/>                   | <dl> <dt>Textstor. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>Textstor. idl</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**ITextStoreACP:: InsertEmbedded**](/windows/desktop/api/Textstor/nf-textstor-itextstoreacp-insertembedded)
</dt> </dl>

 

