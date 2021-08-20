---
description: 'Altre informazioni su: JET_PFNSTATUS delegato'
title: JET_PFNSTATUS delegato
TOCTitle: JET_PFNSTATUS delegate
ms:assetid: T:Microsoft.Isam.Esent.Interop.JET_PFNSTATUS
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_pfnstatus(v=EXCHG.10)
ms:contentKeyID: 39515654
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_PFNSTATUS
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_PFNSTATUS..ctor
- Microsoft.Isam.Esent.Interop.JET_PFNSTATUS.EndInvoke
- Microsoft.Isam.Esent.Interop.JET_PFNSTATUS.Invoke
- Microsoft.Isam.Esent.Interop.JET_PFNSTATUS
- Microsoft.Isam.Esent.Interop.JET_PFNSTATUS.BeginInvoke
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 90aef128f5fdbfdd63d445a07883cc2563311a48092afe4af6cc6cb955d4d609
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117893463"
---
# <a name="jet_pfnstatus-delegate"></a>JET_PFNSTATUS delegato

Riceve informazioni sullo stato di avanzamento delle operazioni a esecuzione lunga, ad esempio le operazioni di deframmentazione, backup o ripristino. Durante tali operazioni, il motore di database chiama questa funzione di callback per fornire un aggiornamento sullo stato di avanzamento dell'operazione.

**Spazio dei**  [nomi: Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Sintassi

``` vb
'Declaration
Public Delegate Function JET_PFNSTATUS ( _
    sesid As JET_SESID, _
    snp As JET_SNP, _
    snt As JET_SNT, _
    data As Object _
) As JET_err
'Usage
Dim instance As New JET_PFNSTATUS(AddressOf HandlerMethod)
```

``` csharp
public delegate JET_err JET_PFNSTATUS(
    JET_SESID sesid,
    JET_SNP snp,
    JET_SNT snt,
    Object data
)
```

#### <a name="parameters"></a>Parametri

  - sesid  
    Tipo: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)  
    
    Sessione con cui è stata chiamata l'operazione a esecuzione lunga.

<!-- end list -->

  - Snp  
    Tipo: [Microsoft.Isam.Esent.Interop.JET_SNP](./jet-snp-enumeration.md)  
    
    Tipo di operazione.

<!-- end list -->

  - Snt  
    Tipo: [Microsoft.Isam.Esent.Interop.JET_SNT](./jet-snt-enumeration.md)  
    
    Stato dell'operazione.

<!-- end list -->

  - data  
    Tipo: [System.Object](/dotnet/api/system.object)  
    
    Dati facoltativi. Può essere un [JET_SNPROG](./jet-snprog-class.md).

#### <a name="return-value"></a>Valore restituito

Tipo: [Microsoft.Isam.Esent.Interop.JET_err](./jet-err-enumeration.md)  

## <a name="see-also"></a>Vedi anche

#### <a name="reference"></a>Riferimento

[Spazio dei nomi Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)
