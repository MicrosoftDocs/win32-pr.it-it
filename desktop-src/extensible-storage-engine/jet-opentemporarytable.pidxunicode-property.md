---
description: 'Altre informazioni su: JET_OPENTEMPORARYTABLE.pidxunicode'
title: JET_OPENTEMPORARYTABLE.pidxunicode (Microsoft.Isam.Esent.Interop.Vista)
TOCTitle: 'pidxunicode property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.Vista.JET_OPENTEMPORARYTABLE.pidxunicode
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.vista.jet_opentemporarytable.pidxunicode(v=EXCHG.10)
ms:contentKeyID: 55104227
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Vista.JET_OPENTEMPORARYTABLE.pidxunicode
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Vista.JET_OPENTEMPORARYTABLE.set_pidxunicode
- Microsoft.Isam.Esent.Interop.Vista.JET_OPENTEMPORARYTABLE.get_pidxunicode
- Microsoft.Isam.Esent.Interop.Vista.JET_OPENTEMPORARYTABLE.pidxunicode
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 378c1497d57e3d904398d92d654579cc4a8702271db3525a2943e50ae3d03726
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118074025"
---
# <a name="jet_opentemporarytablepidxunicode-property"></a>JET_OPENTEMPORARYTABLE.pidxunicode

Ottiene o imposta l'ID delle impostazioni locali e i flag di normalizzazione da utilizzare per confrontare i dati delle colonne chiave Unicode nella tabella temporanea. Quando questo parametro è Null, verrà usato l'LCID predefinito per confrontare le colonne chiave Unicode nella tabella temporanea. L'LCID predefinito è l'inglese degli Stati Uniti. Quando questo parametro è Null, verranno usati i flag di normalizzazione predefiniti per confrontare i dati delle colonne chiave Unicode nella tabella temporanea. I flag di normalizzazione predefiniti sono: NORM_IGNORECASE, NORM_IGNOREKANATYPE e NORM_IGNOREWIDTH.

**Spazio dei nomi:**  [Microsoft.Isam.Esent.Interop.Vista](./microsoft.isam.esent.interop.vista-namespace.md)  
**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Sintassi

``` vb
'Declaration
Public Property pidxunicode As JET_UNICODEINDEX
    Get
    Set
'Usage
Dim instance As JET_OPENTEMPORARYTABLE
Dim value As JET_UNICODEINDEX

value = instance.pidxunicode

instance.pidxunicode = value
```

``` csharp
public JET_UNICODEINDEX pidxunicode { get; set; }
```

#### <a name="property-value"></a>Valore proprietà

Tipo: [Microsoft.Isam.Esent.Interop.JET_UNICODEINDEX](./jet-unicodeindex-class.md)  

## <a name="see-also"></a>Vedi anche

#### <a name="reference"></a>Riferimento

[JET_OPENTEMPORARYTABLE classe](./jet-opentemporarytable-class.md)

[JET_OPENTEMPORARYTABLE membri](./jet-opentemporarytable-members.md)

[Spazio dei nomi Microsoft.Isam.Esent.Interop.Vista](./microsoft.isam.esent.interop.vista-namespace.md)
