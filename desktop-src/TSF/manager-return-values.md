---
title: Valori restituiti da Manager (Msctf.h)
description: Il Framework servizi di testo produce valori restituiti nell'intervallo compreso tra 0xHHHH0200 e 0xHHHH0507. La tabella seguente fornisce i valori restituiti dal manager in ordine alfabetico.
ms.assetid: 12178252-c246-4fa4-bf7b-2445b859ec01
topic_type:
- apiref
api_name:
- Manager Return Values
api_location:
- Msctf.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ac9e914e393a136205a0e1bb3338c43c4cbb6a9dbaf75dad43255eeac2f999f6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118876678"
---
# <a name="manager-return-values"></a>Valori restituiti dal gestore

Il Framework servizi di testo produce valori restituiti nell'intervallo compreso tra 0x *HHHH* 0200 e 0x *HHHH* 0507. La tabella seguente fornisce i valori restituiti dal manager in ordine alfabetico.

> [!Note]  
> Le descrizioni fornite non sono specifiche. Il significato di un valore restituito può variare a seconda del metodo che ha restituito il valore.

 



| Codice/valore restituito                                                                                                                                                                                                                                                   | Descrizione                                                                                       |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------|
| <span id="TF_E_ALREADY_EXISTS"></span><span id="tf_e_already_exists"></span><dl> <dt>**TF \_ E \_ ALREADY \_ EXISTS**</dt> <dt>0x80040506</dt> </dl>                   | La chiave mantenuta è registrata.<br/>                                                       |
| <span id="TF_E_COMPOSITION_REJECTED"></span><span id="tf_e_composition_rejected"></span><dl> <dt>**TF \_ E \_ COMPOSITION \_ REJECTED**</dt> <dt>0x80040508</dt> </dl> | Il proprietario del contesto ha rifiutato la composizione.<br/>                                            |
| <span id="TF_E_DISCONNECTED"></span><span id="tf_e_disconnected"></span><dl> <dt>**TF \_ E \_ DISCONNECTED**</dt> <dt>0x80040504</dt> </dl>                          | L'oggetto contesto non si trova in uno stack di documenti.<br/>                                         |
| <span id="TF_E_EMPTYCONTEXT"></span><span id="tf_e_emptycontext"></span><dl> <dt>**TF \_ E \_ EMPTYCONTEXT**</dt> <dt>0x80040509</dt> </dl>                          | Il contesto è vuoto.<br/>                                                                  |
| <span id="TF_E_FORMAT"></span><span id="tf_e_format"></span><dl> <dt>**TF \_ E \_ FORMAT**</dt> <dt>0x8004020a</dt> </dl>                                            | Il proprietario del contesto non può gestire oggetti del tipo fornito dal parametro pDataObject.<br/> |
| <span id="TF_E_INVALIDPOINT"></span><span id="tf_e_invalidpoint"></span><dl> <dt>**TF \_ E \_ INVALIDPOINT**</dt> <dt>0x80040207</dt> </dl>                          | Le coordinate dello schermo non sono valide.<br/>                                                    |
| <span id="TF_E_INVALIDPOS"></span><span id="tf_e_invalidpos"></span><dl> <dt>**TF \_ E \_ INVALIDPOS**</dt> <dt>0x80040200</dt> </dl>                                | La posizione del carattere non è valida.<br/>                                                     |
| <span id="TF_E_INVALIDVIEW"></span><span id="tf_e_invalidview"></span><dl> <dt>**TF \_ E \_ INVALIDVIEW**</dt> <dt>0x80040505</dt> </dl>                             | La visualizzazione del contesto non è valida.<br/>                                                           |
| <span id="TF_E_LOCKED"></span><span id="tf_e_locked"></span><dl> <dt>**TF \_ E \_ BLOCCO**</dt> <dt>0x80040500</dt> </dl>                                            | Il contesto è già bloccato.<br/>                                                         |
| <span id="TF_E_NOINTERFACE"></span><span id="tf_e_nointerface"></span><dl> <dt>**TF \_ E \_ NOINTERFACE**</dt> <dt>0x80040204</dt> </dl>                             | L'oggetto non supporta l'interfaccia richiesta.<br/>                                   |
| <span id="TF_E_NOLAYOUT"></span><span id="tf_e_nolayout"></span><dl> <dt>**TF \_ E \_ NOLAYOUT**</dt> <dt>0x80040206</dt> </dl>                                      | Il layout del testo non è stato calcolato.<br/>                                               |
| <span id="TF_E_NOLOCK"></span><span id="tf_e_nolock"></span><dl> <dt>**TF \_ E \_ NOLOCK**</dt> <dt>0x80040201</dt> </dl>                                            | Il chiamante non dispone del tipo di documento necessario.<br/>                               |
| <span id="TF_E_NOOBJECT"></span><span id="tf_e_noobject"></span><dl> <dt>**TF \_ E \_ NOOBJECT**</dt> <dt>0x80040202</dt> </dl>                                      | Nella posizione specificata non esiste alcun oggetto incorporato.<br/>                                   |
| <span id="TF_E_NOPROVIDER"></span><span id="tf_e_noprovider"></span><dl> <dt>**TF \_ E \_ NOPROVIDER**</dt> <dt>0x80040503</dt> </dl>                                | Non esiste alcun provider di funzioni per la funzione specificata.<br/>                                |
| <span id="TF_E_NOSELECTION"></span><span id="tf_e_noselection"></span><dl> <dt>**TF \_ E \_ NOSELECTION**</dt> <dt>0x80040205</dt> </dl>                             | Non esiste alcuna selezione all'interno del contesto.<br/>                                                |
| <span id="TF_E_NOSERVICE"></span><span id="tf_e_noservice"></span><dl> <dt>**TF \_ E \_ NOSERVICE**</dt> <dt>0x80040203</dt> </dl>                                   | Il servizio specificato non esiste o non può essere creato.<br/>                            |
| <span id="TF_E_NOTOWNEDRANGE"></span><span id="tf_e_notownedrange"></span><dl> <dt>**TF \_ E \_ NO NAMEDRANGE**</dt> <dt>0x80040502</dt> </dl>                       | Il gestore TSF non è proprietario dell'intervallo.<br/>                                                |
| <span id="TF_E_RANGE_NOT_COVERED"></span><span id="tf_e_range_not_covered"></span><dl> <dt>**TF \_ INTERVALLO \_ E \_ NON \_ COPERTO**</dt> <dt>0X80040507</dt> </dl>         | L'intervallo non è all'interno di una composizione attiva.<br/>                                         |
| <span id="TF_E_READONLY"></span><span id="tf_e_readonly"></span><dl> <dt>**TF \_ E \_ READONLY**</dt> <dt>0x80040209</dt> </dl>                                      | Il contesto di modifica è di sola lettura.<br/>                                                         |
| <span id="TF_E_STACKFULL"></span><span id="tf_e_stackfull"></span><dl> <dt>**TF \_ E \_ STACKFULL**</dt> <dt>0x80040501</dt> </dl>                                   | Lo stack di contesto è pieno.<br/>                                                             |
| <span id="TF_E_SYNCHRONOUS"></span><span id="tf_e_synchronous"></span><dl> <dt>**TF \_ E \_ SINCRONO**</dt> <dt>0x80040208</dt> </dl>                             | Non è possibile ottenere un blocco sincrono di sola lettura.<br/>                                       |
| <span id="TF_S_ASYNC"></span><span id="tf_s_async"></span><dl> <dt>**TF \_ S \_ ASYNC**</dt> <dt>0x00040300</dt> </dl>                                               | I dati verranno ottenuti in modo asincrono.<br/>                                              |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                           |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                 |
| Componente ridistribuibile<br/>          | TSF 1.0 in Windows 2000 Professional<br/>                                      |
| Intestazione<br/>                   | <dl> <dt>Msctf.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>Msctf.idl</dt> </dl> |



 

 





