---
description: 'Altre informazioni su: Proprietà EsentErrorException. Error'
title: Proprietà EsentErrorException. Error
TOCTitle: 'Error property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.EsentErrorException.Error
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esenterrorexception.error(v=EXCHG.10)
ms:contentKeyID: 55101646
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentErrorException.Error
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentErrorException.get_Error
- Microsoft.Isam.Esent.Interop.EsentErrorException.Error
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: e777886ed95ea72a02626f7eb91724123a495f24
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104233760"
---
# <a name="esenterrorexceptionerror-property"></a>Proprietà EsentErrorException. Error

Ottiene l'errore ESENT sottostante per questa eccezione.

**Spazio dei nomi:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft. ISAM. esent. Interop (in Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Sintassi

``` vb
'Declaration
Public ReadOnly Property Error As JET_err
    Get
'Usage
Dim instance As EsentErrorException
Dim value As JET_err

value = instance.Error
```

``` csharp
public JET_err Error { get; }
```

#### <a name="property-value"></a>Valore proprietà

Tipo: [Microsoft.ISAM.esent.Interop.JET_err](./jet-err-enumeration.md)  

## <a name="see-also"></a>Vedi anche

#### <a name="reference"></a>Riferimento

[Classe EsentErrorException](./esenterrorexception-class.md)

[Membri di EsentErrorException](./esenterrorexception-members.md)

[Spazio dei nomi Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)
