---
description: La \_ proprietà NewEnum di OID recupera un'interfaccia IEnumVARIANT su un oggetto che può essere utilizzato per enumerare la raccolta. Questa proprietà è nascosta all'interno di Visual Basic Scripting Edition (VBScript).
ms.assetid: 7c09fd11-064b-451e-bd6b-e6c13ab228a0
title: Proprietà OIDs._NewEnum
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
ms.openlocfilehash: d20856c17dda18a10b85c01453cbe043144742d4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106325158"
---
# <a name="oids_newenum-property"></a>OID. \_ Proprietà NewEnum

\[La proprietà **\_ NewEnum** è disponibile per l'uso nei sistemi operativi specificati nella sezione requisiti. Usare invece la [**classe OidCollection**](/dotnet/api/system.security.cryptography.oidcollection?view=netcore-3.1) nello spazio dei nomi [**System. Security. Cryptography**](/dotnet/api/system.security.cryptography?view=dotnet-plat-ext-3.1&preserve-view=true) .\]

La proprietà **\_ NewEnum** recupera un'interfaccia [**IEnumVARIANT**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) su un oggetto che può essere utilizzato per enumerare la raccolta. Questa proprietà è nascosta all'interno di Visual Basic Scripting Edition (VBScript).

## <a name="syntax"></a>Sintassi


```VB
OIDs._NewEnum As IUnknown
```



## <a name="property-value"></a>Valore proprietà

Interfaccia [**IEnumVARIANT**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) su un oggetto che può essere utilizzato per enumerare la raccolta.

## <a name="remarks"></a>Commenti

Questa proprietà viene automaticamente utilizzata internamente quando si utilizza il `For Each In` costrutto in Visual Basic Scripting Edition (VBScript).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|----------------------------|----------------------------------------------------------------------------------------|
| Componente ridistribuibile<br/> | CAPICOM 2,0 o versioni successive in Windows Server 2003 e Windows XP<br/>                  |
| DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**OID**](oids.md)
</dt> </dl>

 

 
