---
description: La \_ proprietà NewEnum dei firmatari recupera un'interfaccia IEnumVARIANT su un oggetto che può essere usato per enumerare la raccolta. Questa proprietà è nascosta in Visual Basic Scripting Edition (VBScript).
ms.assetid: 99d7ddd3-a552-4125-b220-d1b28f20d1ed
title: Signers._NewEnum proprietà
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Signers._NewEnum
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 866b85d8bfd5eee89a8c8766acb10baa024aa35e4f81b7d7289a6430d345fa6c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118898398"
---
# <a name="signers_newenum-property"></a>Firmatari. \_ NewEnum - proprietà

\[La **\_ proprietà NewEnum** è disponibile per l'uso nei sistemi operativi specificati nella sezione Requisiti. Usare invece una raccolta di oggetti CmsSigner. Per altre informazioni, vedere la [**classe CmsSigner**](/dotnet/api/system.security.cryptography.pkcs.cmssigner?view=dotnet-plat-ext-3.1&preserve-view=true) nello spazio dei [**nomi System.Security.Cryptography.Pkcs.**](/dotnet/api/system.security.cryptography.pkcs?view=dotnet-plat-ext-3.1&preserve-view=true)\]

La **\_ proprietà NewEnum** recupera [**un'interfaccia IEnumVARIANT**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) su un oggetto che può essere usato per enumerare la raccolta. Questa proprietà è nascosta in Visual Basic Scripting Edition (VBScript).

## <a name="syntax"></a>Sintassi


```VB
Signers._NewEnum As IUnknown
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

[**Firmatari**](signers.md)
</dt> </dl>

 

 
