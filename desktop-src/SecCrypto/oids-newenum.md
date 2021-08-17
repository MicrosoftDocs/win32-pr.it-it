---
description: La \_ proprietà NewEnum degli OID recupera un'interfaccia IEnumVARIANT su un oggetto che può essere usato per enumerare la raccolta. Questa proprietà è nascosta in Visual Basic Scripting Edition (VBScript).
ms.assetid: 7c09fd11-064b-451e-bd6b-e6c13ab228a0
title: OIDs._NewEnum proprietà
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- OIDs._NewEnum
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 9d7841f2b041a9e48f9954b1f81d68828e1bef17f16d7f54e470ab2ecb904916
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117979490"
---
# <a name="oids_newenum-property"></a>OID. \_ NewEnum - proprietà

\[La **\_ proprietà NewEnum** è disponibile per l'uso nei sistemi operativi specificati nella sezione Requisiti. Usare invece la [**classe OidCollection nello**](/dotnet/api/system.security.cryptography.oidcollection?view=netcore-3.1) spazio [**dei nomi System.Security.Cryptography.**](/dotnet/api/system.security.cryptography?view=dotnet-plat-ext-3.1&preserve-view=true)\]

La **\_ proprietà NewEnum** recupera [**un'interfaccia IEnumVARIANT**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) su un oggetto che può essere usato per enumerare la raccolta. Questa proprietà è nascosta in Visual Basic Scripting Edition (VBScript).

## <a name="syntax"></a>Sintassi


```VB
OIDs._NewEnum As IUnknown
```



## <a name="property-value"></a>Valore proprietà

Interfaccia [**IEnumVARIANT su**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) un oggetto che può essere utilizzata per enumerare la raccolta.

## <a name="remarks"></a>Commenti

Questa proprietà viene usata automaticamente internamente quando si usa il `For Each In` costrutto in Visual Basic Scripting Edition (VBScript).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|----------------------------|----------------------------------------------------------------------------------------|
| Componente ridistribuibile<br/> | CAPICOM 2.0 o versioni successive in Windows Server 2003 e Windows XP<br/>                  |
| DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Oid**](oids.md)
</dt> </dl>

 

 
