---
title: Proprietà predefinite (msctf. h)
description: I valori seguenti identificano le proprietà definite da TSF. Il formato dei dati e il contenuto di ogni tipo di proprietà sono inclusi.
ms.assetid: d88f2eba-4c98-4b32-96e1-cd019fe0f7ad
keywords:
- Framework servizi di testo proprietà predefinite
topic_type:
- apiref
api_name:
- Predefined Properties
api_location:
- Msctf.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 807d1be5d1cc025971ad294fac825b89a4a0a519
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106302239"
---
# <a name="predefined-properties"></a>Proprietà predefinite

I valori seguenti identificano le proprietà definite da TSF. Il formato dei dati e il contenuto di ogni tipo di proprietà sono inclusi.

## <a name="properties"></a>Proprietà



| Proprietà                        | Descrizione                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
|---------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **\_attributo GUID Prop \_**       | Contiene un valore [**TfGuidAtom**](tfguidatom.md) che rappresenta il **GUID** dell'attributo di visualizzazione. [**ITfCategoryMgr:: GetGuid**](/windows/desktop/api/Msctf/nf-msctf-itfcategorymgr-getguid) viene usato per convertire questo valore in un **GUID**. Per ulteriori informazioni, vedere [utilizzo degli attributi di visualizzazione](using-display-attributes.md).                                                                                                                                                                                                                                                                                                                                                                             |
| **GUID \_ prop \_ TEXTOWNER**       | Contiene un valore [**TfGuidAtom**](tfguidatom.md) che rappresenta l'identificatore di classe ( **CLSID** ) del servizio di testo proprietario del testo. [**ITfCategoryMgr:: GetGuid**](/windows/desktop/api/Msctf/nf-msctf-itfcategorymgr-getguid) viene usato per convertire questo valore in un **CLSID**.                                                                                                                                                                                                                                                                                                                                                                                                                            |
| **GUID \_ prop \_ LangID**          | Contiene un valore **DWORD** che contiene l'identificatore di lingua ( **LangID** ) del testo nella parola bassa.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| **\_lettura della prop GUID \_**         | Contiene il testo di lettura fonetica per il testo coperto dalla proprietà. Questa operazione può essere diversa dal testo effettivo. Questa proprietà non è supportata nelle app di Windows Store.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| **\_composizione della prop GUID \_**       | Contiene un valore booleano che è diverso da zero se il testo fa parte di una composizione o zero in caso contrario. Se questa proprietà è VT \_ vuota, si può presupporre che il testo non faccia parte di una composizione.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| **GUID \_ prop \_ MODEBIAS**        | Contiene un valore [**TfGuidAtom**](tfguidatom.md) che rappresenta il tipo di distorsione della modalità supportata. [**ITfCategoryMgr:: GetGuid**](/windows/desktop/api/Msctf/nf-msctf-itfcategorymgr-getguid) viene usato per convertire questo valore in un **GUID**. Può trattarsi di uno dei [**valori di distorsione della modalità**](mode-bias-values.md).                                                                                                                                                                                                                                                                                                                                                                                                  |
| **GUID \_ prop \_ Love My lifeATTICE**       | Contiene un puntatore a un oggetto [**ITfLMLattice**](/windows/desktop/api/Ctffunc/nn-ctffunc-itflmlattice) .                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| **GUID \_ prop \_ TKB \_ alternative** | **A partire da Windows 8:** Contiene un valore **DWORD** impostato dalla tastiera touch. Questa proprietà può essere usata dai controlli di modifica compatibili con TSF e dalle app per identificare la natura del testo nell'intervallo di testo incluso nella proprietà, ad esempio se il testo nell'intervallo risulta dall'inserimento di un suggerimento di testo o di correzione automatica. <br/> La natura del testo nell'intervallo di testo coperto dalla proprietà si estende anche al tipo di alternative che verrebbero restituite dall'interfaccia [**ITfFnReconversion**](/windows/desktop/api/Ctffunc/nn-ctffunc-itffnreconversion) per l'intervallo di testo nel documento.<br/> Per i valori possibili di questa proprietà, vedere i seguenti commenti.<br/> |



 

## <a name="remarks"></a>Commenti

La proprietà **GUID \_ prop \_ TKB \_ alternates** può essere uno dei valori seguenti.



| Nome                                     | Valore      | Descrizione                                                                                                                                                                                                                                                                                                                                                                                                                                       |
|------------------------------------------|------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| TKB \_ alternations \_ standard                | 0x00000001 | Indica che la tastiera touch ha generato un elenco di possibili parole alternative per il testo nell'intervallo coperto dalla proprietà e che né l'intervallo di testo né le alternative sono una correzione automatica o un suggerimento di testo.                                                                                                                                                                                                              |
| TKB \_ alternative \_ per la \_ correzione automatica     | 0x00000002 | Indica che la tastiera touch ha generato una parola alternativa che sostituisce automaticamente il testo nell'intervallo di testo coperto dalla proprietà.<br/> La tastiera touch non applica la correzione automatica senza che venga richiesto di eseguire questa operazione dal controllo o dall'app di modifica. L'interfaccia di riconversione ([**ITfFnReconversion**](/windows/desktop/api/Ctffunc/nn-ctffunc-itffnreconversion)) deve essere utilizzata per applicare la correzione al testo nel documento.<br/> |
| TKB \_ alternative \_ per la \_ stima         | 0x00000003 | Indica che l'intervallo di testo coperto dalla proprietà è un suggerimento di testo generato dalla tastiera a tocco e inserito nel documento dall'utente.<br/> Le stime alternative aggiuntive possono essere archiviate anche come proprietà nel documento.<br/>                                                                                                                                                                     |
| TKB \_ alterna la \_ correzione automatica \_ applicata | 0x00000004 | Indica che l'intervallo di testo coperto dalla proprietà è una correzione automatica fornita dalla tastiera a tocco e applicata tramite l'interfaccia [**ITfFnReconversion**](/windows/desktop/api/Ctffunc/nn-ctffunc-itffnreconversion) .<br/> Questo valore può essere usato dai controlli di modifica o dalle app, con TKB \_ alternative \_ per \_ la correzione automatica, per impedire l'applicazione ripetuta di una correzione automatica.<br/>                                                                               |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                           |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                 |
| Componente ridistribuibile<br/>          | TSF 1,0 su Windows 2000 Professional<br/>                                      |
| Intestazione<br/>                   | <dl> <dt>Msctf. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>Msctf. idl</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**TfGuidAtom**](tfguidatom.md)
</dt> <dt>

[**ITfCategoryMgr:: GetGuid**](/windows/desktop/api/Msctf/nf-msctf-itfcategorymgr-getguid)
</dt> <dt>

[Utilizzo degli attributi di visualizzazione](using-display-attributes.md)
</dt> <dt>

[**Valori di distorsione della modalità**](mode-bias-values.md)
</dt> <dt>

[**ITfLMLattice**](/windows/desktop/api/Ctffunc/nn-ctffunc-itflmlattice)
</dt> </dl>

 

 





