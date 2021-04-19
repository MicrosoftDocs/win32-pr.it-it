---
description: La proprietà Property dell'oggetto SummaryInfo imposta o ottiene il valore per la proprietà specificata nel flusso di informazioni di riepilogo.
ms.assetid: 8e8f0987-c92b-43f3-a61a-35099188c629
title: Proprietà SummaryInfo. Property
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SummaryInfo.Property
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 0e51773a930b8868e31a7e88848300a62b717912
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106327309"
---
# <a name="summaryinfoproperty-property"></a>Proprietà SummaryInfo. Property

La proprietà **Property** dell'oggetto [**SummaryInfo**](summaryinfo-object.md) imposta o ottiene il valore per la proprietà specificata nel flusso di informazioni di riepilogo. Le proprietà vengono lette quando viene creato l'oggetto [**SummaryInfo**](summaryinfo-object.md) , ma non vengono scritte fino a quando non viene chiamato il metodo di [**salvataggio permanente**](summaryinfo-persist.md) . L'impostazione di una proprietà su Empty ne causa la rimozione. Analogamente, la richiesta di una proprietà inesistente restituisce un valore vuoto. In caso contrario, i valori possono essere trasferiti come stringhe, numeri interi o tipi di data (data e ora).

Questa proprietà è di sola lettura.

## <a name="syntax"></a>Sintassi


```JScript
propVal = SummaryInfo.Property
```



## <a name="property-value"></a>Valore proprietà

ID di proprietà obbligatorio di una delle proprietà di riepilogo.

## <a name="remarks"></a>Commenti

**ID di proprietà di riepilogo standard**

(non un'enumerazione)



| Nome parametro     | valore | Descrizione                                       |
|--------------------|-------|---------------------------------------------------|
| \_dizionario PID    | 0     | Formato speciale, non supportato dall'oggetto SummaryInfo |
| tabella \_ codici PID      | 1     | \_I2 VT                                            |
| \_titolo PID         | 2     | \_LPSTR VT                                         |
| \_oggetto PID       | 3     | \_LPSTR VT                                         |
| \_autore PID        | 4     | \_LPSTR VT                                         |
| \_parole chiave PID      | 5     | \_LPSTR VT                                         |
| \_Commenti PID      | 6     | \_LPSTR VT                                         |
| \_modello PID      | 7     | \_LPSTR VT                                         |
| \_LASTAUTHOR PID    | 8     | \_LPSTR VT                                         |
| \_REVNUMBER PID     | 9     | \_LPSTR VT                                         |
| \_EDITTIME PID      | 10    | FILETIME VT \_                                      |
| \_LASTPRINTED PID   | 11    | FILETIME VT \_                                      |
| PID \_ creare il \_ DTM   | 12    | FILETIME VT \_                                      |
| PID \_ LASTSAVE \_ DTM | 13    | FILETIME VT \_                                      |
| \_PageCount PID     | 14    | VT \_ I4                                            |
| \_WORDCOUNT PID     | 15    | VT \_ I4                                            |
| \_charCount PID     | 16    | VT \_ I4                                            |
| \_Anteprima PID     | 17    | VT \_ CF (non supportato)                            |
| \_appname PID       | 18    | \_LPSTR VT                                         |
| \_sicurezza PID      | 19    | VT \_ I4                                            |



 

**Tipi di dati delle proprietà**

(non un'enumerazione)



| Nome parametro | valore | Descrizione                                                                              |
|----------------|-------|------------------------------------------------------------------------------------------|
| \_I2 VT         | 2     | intero a 16 bit                                                                           |
| VT \_ I4         | 3     | Intero a 32 bit                                                                           |
| \_LPSTR VT      | 30    | string                                                                                   |
| FILETIME VT \_   | 64    | Data/ora (FILETIME, convertita in ora Variant)                                          |
| VT \_ CF         | 71    | Formato degli Appunti + dati, non gestiti dall'oggetto [**SummaryInfo**](summaryinfo-object.md) |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versione<br/> | Windows Installer 5,0 in Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Installer 4,0 o Windows Installer 4,5 in Windows Server 2008 o Windows Vista. Windows Installer in Windows Server 2003 o Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ ISummaryInfo è definito come 000C109B-0000-0000-C000-000000000046<br/>                                                                                                                                                                         |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**MsiSummaryInfoSetProperty**](/windows/desktop/api/Msiquery/nf-msiquery-msisummaryinfosetpropertya)
</dt> <dt>

[**MsiSummaryInfoGetProperty**](/windows/desktop/api/Msiquery/nf-msiquery-msisummaryinfogetpropertya)
</dt> </dl>

 

 




