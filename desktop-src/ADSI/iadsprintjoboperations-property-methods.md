---
title: Metodi della proprietà IADsPrintJobOperations (Iads.h)
description: I metodi di proprietà dell'interfaccia IADsPrintJobOperations leggono e scrivono le proprietà elencate nella tabella seguente. Per altre informazioni sui metodi di proprietà, vedere Metodi delle proprietà di interfaccia.
ms.assetid: d1710bd4-e600-4d92-892a-16b4316851d4
ms.tgt_platform: multiple
keywords:
- Metodi della proprietà IADsPrintJobOperations ADSI
topic_type:
- apiref
api_name:
- IADsPrintJobOperations Property Methods
- IADsPrintJobOperations.Status
- IADsPrintJobOperations.get_Status
- IADsPrintJobOperations.TimeElapsed
- IADsPrintJobOperations.get_TimeElapsed
- IADsPrintJobOperations.PagesPrinted
- IADsPrintJobOperations.get_PagesPrinted
- IADsPrintJobOperations.Position
- IADsPrintJobOperations.get_Position
- IADsPrintJobOperations.put_Position
api_location:
- Activeds.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 70f337681cb7e75a478000bd06daaac1165edaaaf1cb4255b2890347fbcff7de
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118691070"
---
# <a name="iadsprintjoboperations-property-methods"></a>Metodi della proprietà IADsPrintJobOperations

I metodi di proprietà [**dell'interfaccia IADsPrintJobOperations**](/windows/desktop/api/Iads/nn-iads-iadsprintjoboperations) leggono e scrivono le proprietà elencate nella tabella seguente. Per altre informazioni sui metodi di proprietà, vedere [Metodi delle proprietà di interfaccia.](interface-property-methods.md)

## <a name="properties"></a>Proprietà

<dl> <dt>

**Pagine stampate**
</dt> <dd> <dl>

Contiene il numero di pagine stampate.

<dt>

Tipo di accesso: sola lettura
</dt> <dt>

Tipo di dati di scripting: **LONG**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_PagesPrinted(
  [out] LONG* plPagesPrinted
);
```


</dt> </dl> </dd> <dt>

**Position**
</dt> <dd> <dl>

Contiene la posizione di questo processo di stampa nella coda di stampa.

<dt>

Tipo di accesso: Lettura/scrittura
</dt> <dt>

Tipo di dati di scripting: **LONG**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Position(
  [out] LONG* plPosition
);
HRESULT put_Position(
  [in] LONG lPosition
);
```


</dt> </dl> </dd> <dt>

**Status**
</dt> <dd> <dl>

Contiene lo stato corrente del processo di stampa come indicato da una delle costanti dello stato del processo [**di stampa ADSI.**](adsi-print-job-status-constants.md)

<dt>

Tipo di accesso: sola lettura
</dt> <dt>

Tipo di dati di scripting: **LONG**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Status(
  [out] LONG* plStatus
);
```


</dt> </dl> </dd> <dt>

**TimeElapsed**
</dt> <dd> <dl>

Contiene il numero di millisecondi trascorsi dall'avvio del processo di stampa.

<dt>

Tipo di accesso: sola lettura
</dt> <dt>

Tipo di dati di scripting: **LONG**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_TimeElapsed(
  [out] LONG* plTimeElapsed
);
```


</dt> </dl> </dd> </dl>

 

## <a name="examples"></a>Esempio

L'esempio di codice seguente illustra come usare le proprietà [**per IADsPrintJobOperations.**](/windows/desktop/api/Iads/nn-iads-iadsprintjoboperations)


```VB
Dim pqo As IADsPrintQueueOperations
Dim pjo As IADsPrintJobOperations

On Error GoTo Cleanup

Set pqo = GetObject("WinNT://aMachine/aPrinter")
For Each pj In pqo.PrintJobs
    Set pjo = pj
    MsgBox pjo.PagesPrinted & " pages printed for job " & pj.Name
    If (pjo.position > 1) Then
        pjo.Position = pjo.status - 1
    End If
Next

Cleanup:
    If (Err.Number<>0) Then
        MsgBox("An error has occurred. " & Err.Number)
    End If
    Set pqo = Nothing
    Set pjo = Nothing
```



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Vista<br/>                                                                  |
| Server minimo supportato<br/> | Windows Server 2008<br/>                                                            |
| Intestazione<br/>                   | <dl> <dt>Iads.h</dt> </dl>         |
| DLL<br/>                      | <dl> <dt>Activeds.dll</dt> </dl>   |
| IID<br/>                      | IID \_ IADsPrintJobOperations è definito come 32FB6780-1ED0-11CF-A988-00AA006BC149<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IADsPrintJob**](/windows/desktop/api/Iads/nn-iads-iadsprintjob)
</dt> <dt>

[**IADsPrintJobOperations**](/windows/desktop/api/Iads/nn-iads-iadsprintjoboperations)
</dt> <dt>

[**IADsPrintQueue**](/windows/desktop/api/Iads/nn-iads-iadsprintqueue)
</dt> <dt>

[**Costanti dello stato del processo di stampa ADSI**](adsi-print-job-status-constants.md)
</dt> </dl>

 

 





