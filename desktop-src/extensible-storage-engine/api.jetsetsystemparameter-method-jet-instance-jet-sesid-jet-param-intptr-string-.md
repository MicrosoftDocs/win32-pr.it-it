---
description: 'Altre informazioni su: metodo API. JetSetSystemParameter (JET_INSTANCE, JET_SESID, JET_param, IntPtr, String)'
title: Metodo API. JetSetSystemParameter (JET_INSTANCE, JET_SESID, JET_param, IntPtr, String)
TOCTitle: JetSetSystemParameter method (JET_INSTANCE, JET_SESID, JET_param, IntPtr, String)
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetSetSystemParameter(Microsoft.Isam.Esent.Interop.JET_INSTANCE,Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_param,System.IntPtr,System.String)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetsetsystemparameter(v=EXCHG.10)
ms:contentKeyID: 55100822
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetSetSystemParameter
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 72a92ea3d6b6d4b828e409cd08b896f54c4aa053
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104232784"
---
# <a name="apijetsetsystemparameter-method-jet_instance-jet_sesid-jet_param-intptr-string"></a>Metodo API. JetSetSystemParameter (JET_INSTANCE, JET_SESID, JET_param, IntPtr, String)

Imposta le opzioni di configurazione del database.

**Spazio dei nomi:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft. ISAM. esent. Interop (in Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Sintassi

``` vb
'Declaration
Public Shared Function JetSetSystemParameter ( _
    instance As JET_INSTANCE, _
    sesid As JET_SESID, _
    paramid As JET_param, _
    paramValue As IntPtr, _
    paramString As String _
) As JET_wrn
'Usage
Dim instance As JET_INSTANCE
Dim sesid As JET_SESID
Dim paramid As JET_param
Dim paramValue As IntPtr
Dim paramString As String
Dim returnValue As JET_wrn

returnValue = Api.JetSetSystemParameter(instance, _
    sesid, paramid, paramValue, paramString)
```

``` csharp
public static JET_wrn JetSetSystemParameter(
    JET_INSTANCE instance,
    JET_SESID sesid,
    JET_param paramid,
    IntPtr paramValue,
    string paramString
)
```

#### <a name="parameters"></a>Parametri

  - instance  
    Tipo: [Microsoft.ISAM.esent.Interop.JET_INSTANCE](./jet-instance-structure.md)  
    
    Istanza su cui impostare l'opzione o [nil](./jet-instance.nil-property.md) per impostare l'opzione su tutte le istanze.

<!-- end list -->

  - sesid  
    Tipo: [Microsoft.ISAM.esent.Interop.JET_SESID](./jet-sesid-structure.md)  
    
    Sessione da utilizzare.

<!-- end list -->

  - paramid  
    Tipo: [Microsoft.ISAM.esent.Interop.JET_param](./jet-param-enumeration.md)  
    
    Parametro da impostare.

<!-- end list -->

  - paramValue  
    Tipo: [System. IntPtr](/dotnet/api/system.intptr)  
    
    Valore del parametro da impostare se il parametro è di tipo Integer.

<!-- end list -->

  - paramString  
    Tipo: [System. String](/dotnet/api/system.string)  
    
    Valore del parametro da impostare se il parametro è un tipo stringa.

#### <a name="return-value"></a>Valore restituito

Tipo: [Microsoft.ISAM.esent.Interop.JET_wrn](./jet-wrn-enumeration.md)  
Codice di avviso ESENT.  

## <a name="see-also"></a>Vedi anche

#### <a name="reference"></a>Riferimento

[Classe API](./api-class.md)

[Membri API](./api-members.md)

[Overload JetSetSystemParameter](./api.jetsetsystemparameter-method.md)

[Spazio dei nomi Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)
