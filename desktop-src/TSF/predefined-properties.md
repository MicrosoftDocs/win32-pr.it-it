---
title: Proprietà predefinite (Msctf.h)
description: I valori seguenti identificano le proprietà definite da TSF. Sono inclusi il formato dei dati e il contenuto di ogni tipo di proprietà.
ms.assetid: d88f2eba-4c98-4b32-96e1-cd019fe0f7ad
keywords:
- Proprietà predefinite Framework servizi di testo
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
ms.openlocfilehash: 5e506f334de8c440319c2bd09dab28b3576fe4ca2e5a2852b610532166a1d0a9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118875976"
---
# <a name="predefined-properties"></a>Proprietà predefinite

I valori seguenti identificano le proprietà definite da TSF. Sono inclusi il formato dei dati e il contenuto di ogni tipo di proprietà.

## <a name="properties"></a>Proprietà



| Proprietà                        | Descrizione                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
|---------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **ATTRIBUTO \_ GUID \_ PROP**       | Contiene un [**valore TfGuidAtom**](tfguidatom.md) che rappresenta il **GUID dell'attributo** di visualizzazione. [**ITfCategoryMgr::GetGUID**](/windows/desktop/api/Msctf/nf-msctf-itfcategorymgr-getguid) viene usato per convertire questo valore in un **GUID**. Per altre informazioni, vedere [Uso degli attributi di visualizzazione.](using-display-attributes.md)                                                                                                                                                                                                                                                                                                                                                                             |
| **GUID \_ PROP \_ TEXTOWNER**       | Contiene un [**valore TfGuidAtom**](tfguidatom.md) che rappresenta l'identificatore di classe ( **CLSID** ) del servizio di testo proprietario del testo. [**ITfCategoryMgr::GetGUID**](/windows/desktop/api/Msctf/nf-msctf-itfcategorymgr-getguid) viene usato per convertire questo valore in un **CLSID.**                                                                                                                                                                                                                                                                                                                                                                                                                            |
| **GUID \_ PROP \_ LANGID**          | Contiene un **valore DWORD** che contiene l'identificatore di lingua ( **LANGID** ) del testo nella parola in basso.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| **LETTURA \_ DELLA PROPRIETÀ GUID \_**         | Contiene il testo di lettura fonetica per il testo coperto dalla proprietà . Può essere diverso dal testo effettivo. Windows Le app dello Store non supportano questa proprietà.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| **CREAZIONE \_ DI PROPRIETÀ \_ GUID**       | Contiene un valore booleano diverso da zero se il testo fa parte di una composizione o zero in caso contrario. Se questa proprietà è VT EMPTY, si può presunire che \_ il testo non fa parte di una composizione.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| **GUID \_ PROP \_ MODEBIAS**        | Contiene un [**valore TfGuidAtom**](tfguidatom.md) che rappresenta il tipo di distorsione della modalità supportata. [**ITfCategoryMgr::GetGUID**](/windows/desktop/api/Msctf/nf-msctf-itfcategorymgr-getguid) viene usato per convertire questo valore in un **GUID**. Può essere uno dei valori [**di distorsione della modalità**](mode-bias-values.md).                                                                                                                                                                                                                                                                                                                                                                                                  |
| **GUID \_ PROP love my \_ lifeATTICE**       | Contiene un puntatore a [**un oggetto ITfLMLattice.**](/windows/desktop/api/Ctffunc/nn-ctffunc-itflmlattice)                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| **GUID \_ PROP \_ TKB \_ ALTERNATES** | **A partire da Windows 8:** Contiene un **valore DWORD** impostato dalla tastiera virtuale. Questa proprietà può essere usata dalle app e dai controlli di modifica con supporto di TSF per identificare la natura del testo nell'intervallo di testo coperto dalla proprietà , ad esempio se il testo nell'intervallo risulta dall'inserimento di un suggerimento di testo o di una correzione automatica. <br/> La natura del testo nell'intervallo di testo coperto dalla proprietà si estende anche al tipo di alternative che verrebbero restituite dall'interfaccia [**ITfFnReconversion**](/windows/desktop/api/Ctffunc/nn-ctffunc-itffnreconversion) per tale intervallo di testo nel documento.<br/> Per i valori possibili di questa proprietà, vedere le note seguenti.<br/> |



 

## <a name="remarks"></a>Commenti

La **proprietà GUID PROP \_ \_ TKB \_ ALTERNATES** può essere uno dei valori seguenti.



| Nome                                     | Valore      | Descrizione                                                                                                                                                                                                                                                                                                                                                                                                                                       |
|------------------------------------------|------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| TKB \_ ALTERNATES \_ STANDARD                | 0x00000001 | Indica che la tastiera virtuale ha generato un elenco di possibili parole alternative per il testo nell'intervallo coperto dalla proprietà e che né l'intervallo di testo né le alternative sono una correzione automatica o un suggerimento di testo.                                                                                                                                                                                                              |
| ALTERNATIVE TKB \_ \_ PER LA CORREZIONE \_ AUTOMATICA     | 0x00000002 | Indica che la tastiera virtuale ha generato una parola alternativa che deve sostituire automaticamente il testo nell'intervallo di testo coperto dalla proprietà .<br/> La tastiera virtuale non applica la correzione automatica senza che venga richiesto dal controllo di modifica o dall'app. L'interfaccia di riconversione ([**ITfFnReconversion**](/windows/desktop/api/Ctffunc/nn-ctffunc-itffnreconversion)) deve essere usata per applicare la correzione al testo nel documento.<br/> |
| ALTERNATIVE TKB \_ \_ PER LA \_ STIMA         | 0x00000003 | Indica che l'intervallo di testo coperto dalla proprietà è un suggerimento di testo generato dalla tastiera virtuale e inserito nel documento dall'utente.<br/> È anche possibile archiviare stime alternative aggiuntive come proprietà nel documento.<br/>                                                                                                                                                                     |
| CORREZIONE AUTOMATICA ALTERNATIVE TKB \_ \_ \_ APPLICATA | 0x00000004 | Indica che l'intervallo di testo coperto dalla proprietà è una correzione automatica fornita dalla tastiera virtuale e applicata tramite [**l'interfaccia ITfFnReconversion.**](/windows/desktop/api/Ctffunc/nn-ctffunc-itffnreconversion)<br/> Questo valore può essere usato dai controlli di modifica o dalle app, con TKB \_ ALTERNATES \_ FOR AUTOCORRECTION, per impedire l'applicazione ripetuta di una \_ correzione automatica.<br/>                                                                               |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                           |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                 |
| Componente ridistribuibile<br/>          | TSF 1.0 in Windows 2000 Professional<br/>                                      |
| Intestazione<br/>                   | <dl> <dt>Msctf.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>Msctf.idl</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**TfGuidAtom**](tfguidatom.md)
</dt> <dt>

[**ITfCategoryMgr::GetGUID**](/windows/desktop/api/Msctf/nf-msctf-itfcategorymgr-getguid)
</dt> <dt>

[Uso degli attributi di visualizzazione](using-display-attributes.md)
</dt> <dt>

[**Valori distorsione modalità**](mode-bias-values.md)
</dt> <dt>

[**ITfLMLattice**](/windows/desktop/api/Ctffunc/nn-ctffunc-itflmlattice)
</dt> </dl>

 

 





