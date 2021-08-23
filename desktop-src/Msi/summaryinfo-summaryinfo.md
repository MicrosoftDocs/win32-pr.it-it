---
description: La proprietà Property dell'oggetto SummaryInfo imposta o ottiene il valore per la proprietà specificata nel flusso di informazioni di riepilogo.
ms.assetid: 8e8f0987-c92b-43f3-a61a-35099188c629
title: SummaryInfo.Property - proprietà
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
ms.openlocfilehash: 3b8635d081b44adfad3b3e869cb7fab96ee3d81107a8d962153f1caa5a14ac72
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118624094"
---
# <a name="summaryinfoproperty-property"></a>SummaryInfo.Property - proprietà

La **proprietà Property** dell'oggetto [**SummaryInfo**](summaryinfo-object.md) imposta o ottiene il valore per la proprietà specificata nel flusso di informazioni di riepilogo. Le proprietà vengono lette quando viene [**creato l'oggetto SummaryInfo,**](summaryinfo-object.md) ma non vengono scritte fino a quando non viene chiamato il metodo [**Persist.**](summaryinfo-persist.md) L'impostazione di una proprietà su Empty ne causa la rimozione. Analogamente, la richiesta di una proprietà inesistente restituisce un valore Empty. In caso contrario, i valori possono essere trasferiti come stringhe, numeri interi o tipi di data (data/ora).

Questa proprietà è di sola lettura.

## <a name="syntax"></a>Sintassi


```JScript
propVal = SummaryInfo.Property
```



## <a name="property-value"></a>Valore proprietà

ID proprietà obbligatorio di una delle proprietà di riepilogo.

## <a name="remarks"></a>Commenti

**ID delle proprietà di riepilogo standard**

(non un'enumerazione)



| Nome parametro     | valore | Descrizione                                       |
|--------------------|-------|---------------------------------------------------|
| DIZIONARIO \_ PID    | 0     | Formato speciale, non supportato dall'oggetto SummaryInfo |
| TABELLA CODICI \_ PID      | 1     | VT \_ I2                                            |
| TITOLO \_ PID         | 2     | VT \_ LPSTR                                         |
| PID \_ SUBJECT       | 3     | VT \_ LPSTR                                         |
| PID \_ AUTHOR        | 4     | VT \_ LPSTR                                         |
| PAROLE CHIAVE \_ PID      | 5     | VT \_ LPSTR                                         |
| COMMENTI \_ PID      | 6     | VT \_ LPSTR                                         |
| MODELLO \_ PID      | 7     | VT \_ LPSTR                                         |
| PID \_ LASTAUTHOR    | 8     | VT \_ LPSTR                                         |
| PID \_ REVNUMBER     | 9     | VT \_ LPSTR                                         |
| PID \_ EDITTIME      | 10    | VT \_ FILETIME                                      |
| PID \_ LASTPRINTED   | 11    | VT \_ FILETIME                                      |
| PID \_ CREATE \_ DTM   | 12    | VT \_ FILETIME                                      |
| PID \_ LASTSAVE \_ DTM | 13    | VT \_ FILETIME                                      |
| PID \_ PAGECOUNT     | 14    | VT \_ I4                                            |
| PID \_ WORDCOUNT     | 15    | VT \_ I4                                            |
| PID \_ CHARCOUNT     | 16    | VT \_ I4                                            |
| ANTEPRIMA \_ PID     | 17    | VT \_ CF (non supportato)                            |
| PID \_ APPNAME       | 18    | VT \_ LPSTR                                         |
| SICUREZZA \_ PID      | 19    | VT \_ I4                                            |



 

**Tipi di dati delle proprietà**

(non un'enumerazione)



| Nome parametro | valore | Descrizione                                                                              |
|----------------|-------|------------------------------------------------------------------------------------------|
| VT \_ I2         | 2     | Intero a 16 bit                                                                           |
| VT \_ I4         | 3     | Intero a 32 bit                                                                           |
| VT \_ LPSTR      | 30    | string                                                                                   |
| VT \_ FILETIME   | 64    | Data e ora (FILETIME, convertito in ora variant)                                          |
| VT \_ CF         | 71    | Formato degli Appunti + dati, non gestiti [**dall'oggetto SummaryInfo**](summaryinfo-object.md) |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versione<br/> | Windows Programma di installazione 5.0 Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Programma di installazione 4.0 o Windows Installer 4.5 in Windows Server 2008 o Windows Vista. Windows Programma di installazione Windows Server 2003 o Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | ISummaryInfo IID è definito come \_ 000C109B-0000-0000-C000-000000000046<br/>                                                                                                                                                                         |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**MsiSummaryInfoSetProperty**](/windows/desktop/api/Msiquery/nf-msiquery-msisummaryinfosetpropertya)
</dt> <dt>

[**MsiSummaryInfoGetProperty**](/windows/desktop/api/Msiquery/nf-msiquery-msisummaryinfogetpropertya)
</dt> </dl>

 

 




