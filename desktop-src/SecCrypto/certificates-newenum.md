---
description: La \_ proprietà NewEnum di Certificates recupera un'interfaccia IEnumVARIANT su un oggetto che può essere usato per enumerare la raccolta. Questa proprietà è nascosta in Visual Basic Scripting Edition (VBScript).
ms.assetid: bbe6c82c-1949-4d81-bb87-3f05613efa6d
title: Certificates._NewEnum proprietà
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Certificates._NewEnum
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: eab4395e24b12b8e9492c6f18f595a91e192a59c53309411433b49881cd4fd4c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117770513"
---
# <a name="certificates_newenum-property"></a>Certificati. \_ NewEnum - proprietà

\[CAPICOM è un componente solo a 32 bit disponibile per l'uso nei sistemi operativi seguenti: Windows Server 2008, Windows Vista e Windows XP. Usare invece la [**classe X509Certificate2Collection**](/dotnet/api/system.security.cryptography.x509certificates.x509certificate2collection?view=netcore-3.1) nello spazio dei nomi [**System.Security.Cryptography.X509Certificates.**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1)\]

La **\_ proprietà NewEnum** recupera [**un'interfaccia IEnumVARIANT**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) su un oggetto che può essere usato per enumerare la raccolta. Questa proprietà è nascosta in Visual Basic Scripting Edition (VBScript).

## <a name="syntax"></a>Sintassi


```VB
Certificates._NewEnum As IUnknown
```



## <a name="property-value"></a>Valore proprietà

Interfaccia [**IEnumVARIANT**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) su un oggetto che può essere utilizzata per enumerare la raccolta.

## <a name="remarks"></a>Commenti

Questa proprietà viene usata automaticamente internamente quando si usa il `For Each In` costrutto in Visual Basic Scripting Edition (VBScript).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|----------------------------------|----------------------------------------------------------------------------------------|
| Fine del supporto client<br/> | Windows Vista<br/>                                                               |
| Fine del supporto server<br/> | Windows Server 2008<br/>                                                         |
| Componente ridistribuibile<br/>       | CAPICOM 2.0 o versioni successive in Windows Server 2003 e Windows XP<br/>                  |
| DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Certificati**](certificates.md)
</dt> </dl>

 

 
