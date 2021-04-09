---
description: 'Altre informazioni su: metodo API. JetGetSystemParameter (JET_INSTANCE, JET_SESID, JET_param, Int32, String, Int32)'
title: Metodo API. JetGetSystemParameter (JET_INSTANCE, JET_SESID, JET_param, Int32, String, Int32)
TOCTitle: JetGetSystemParameter method (JET_INSTANCE, JET_SESID, JET_param, Int32, String, Int32)
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetGetSystemParameter(Microsoft.Isam.Esent.Interop.JET_INSTANCE,Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_param,System.Int32@,System.String@,System.Int32)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetgetsystemparameter(v=EXCHG.10)
ms:contentKeyID: 55100727
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetGetSystemParameter
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 840c17ef1d74b57b4bee75b9efafe5a314f09a57
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103878873"
---
# <a name="apijetgetsystemparameter-method-jet_instance-jet_sesid-jet_param-int32-string-int32"></a>Metodo API. JetGetSystemParameter (JET_INSTANCE, JET_SESID, JET_param, Int32, String, Int32)

Ottiene le opzioni di configurazione del database.

**Spazio dei nomi:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft. ISAM. esent. Interop (in Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Sintassi

``` vb
'Declaration
Public Shared Function JetGetSystemParameter ( _
    instance As JET_INSTANCE, _
    sesid As JET_SESID, _
    paramid As JET_param, _
    ByRef paramValue As Integer, _
    <OutAttribute> ByRef paramString As String, _
    maxParam As Integer _
) As JET_wrn
'Usage
Dim instance As JET_INSTANCE
Dim sesid As JET_SESID
Dim paramid As JET_param
Dim paramValue As Integer
Dim paramString As String
Dim maxParam As Integer
Dim returnValue As JET_wrn

returnValue = Api.JetGetSystemParameter(instance, _
    sesid, paramid, paramValue, paramString, _
    maxParam)
```

``` csharp
public static JET_wrn JetGetSystemParameter(
    JET_INSTANCE instance,
    JET_SESID sesid,
    JET_param paramid,
    ref int paramValue,
    out string paramString,
    int maxParam
)
```

#### <a name="parameters"></a>Parametri

  - instance  
    Tipo: [Microsoft.ISAM.esent.Interop.JET_INSTANCE](./jet-instance-structure.md)  
    
    Istanza da cui recuperare le opzioni.

<!-- end list -->

  - sesid  
    Tipo: [Microsoft.ISAM.esent.Interop.JET_SESID](./jet-sesid-structure.md)  
    
    Sessione da utilizzare.

<!-- end list -->

  - paramid  
    Tipo: [Microsoft.ISAM.esent.Interop.JET_param](./jet-param-enumeration.md)  
    
    Parametro da ottenere.

<!-- end list -->

  - paramValue  
    Tipo: [System. Int32](/dotnet/api/system.int32)  
    
    Restituisce il valore del parametro, se il valore è un numero intero.

<!-- end list -->

  - paramString  
    Tipo: [System. String](/dotnet/api/system.string)  
    
    Restituisce il valore del parametro, se il valore è una stringa.

<!-- end list -->

  - maxParam  
    Tipo: [System. Int32](/dotnet/api/system.int32)  
    
    Dimensione massima della stringa di parametro.

#### <a name="return-value"></a>Valore restituito

Tipo: [Microsoft.ISAM.esent.Interop.JET_wrn](./jet-wrn-enumeration.md)  
Codice di avviso ESENT.  

## <a name="remarks"></a>Commenti

[ErrorToString](./jet-param-enumeration.md) passa il numero di errore in paramValue, motivo per cui si tratta di un parametro ref e non di un parametro out.

## <a name="see-also"></a>Vedi anche

#### <a name="reference"></a>Riferimento

[Classe API](./api-class.md)

[Membri API](./api-members.md)

[Overload JetGetSystemParameter](./api.jetgetsystemparameter-method.md)

[Spazio dei nomi Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)
