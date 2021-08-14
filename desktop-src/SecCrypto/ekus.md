---
description: Rappresenta una raccolta di oggetti EKU.
ms.assetid: 04b9f0bf-e1d4-4a2c-be5d-bae7c1090bdb
title: Oggetto EKU
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EKUs
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 5258a37ac32e663b45bb2a82f8b0691cca3e1e76c303e8d4f9b7156e4f5a423e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117767084"
---
# <a name="ekus-object"></a>Oggetto EKU

\[CAPICOM è un componente solo a 32 bit disponibile per l'uso nei sistemi operativi seguenti: Windows Server 2008, Windows Vista e Windows XP. Usare invece la [**classe X509ExtensionCollection**](/dotnet/api/system.security.cryptography.x509certificates.x509extensioncollection?view=netcore-3.1) nello spazio dei [**nomi System.Security.Cryptography.X509Certificates.**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1)\]

**L'oggetto EKU** rappresenta una raccolta di [**oggetti EKU.**](eku.md) Ogni [**oggetto EKU**](eku.md) rappresenta una singola proprietà EKU (Extended Key Usage) di un certificato.

## <a name="when-to-use"></a>Utilizzo

La **raccolta EKUs** viene usata per eseguire le attività seguenti:

-   Recuperare il numero di proprietà EKU nella raccolta.
-   Recuperare un [**oggetto EKU**](eku.md) specifico dalla raccolta.
-   Scorrere la raccolta.

## <a name="members"></a>Membri

**L'oggetto EKU** ha questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

**L'oggetto EKU** ha queste proprietà.



| Proprietà                                     | Tipo di accesso          | Descrizione                                                                                                                                                                                                                     |
|:---------------------------------------------|:---------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_NewEnum**](ekus-newenum.md)<br/> | Sola lettura<br/> | Recupera [**un'interfaccia IEnumVARIANT**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) su un oggetto che può essere utilizzato per enumerare la raccolta. Questa proprietà è nascosta in Visual Basic Scripting Edition (VBScript).<br/> |
| [**Conteggio**](ekus-count.md)<br/>       | Sola lettura<br/> | Recupera il numero di [**oggetti EKU**](eku.md) nella raccolta.<br/>                                                                                                                                                |
| [**Elemento**](ekus-item.md)<br/>         | Sola lettura<br/> | Recupera [**l'oggetto EKU**](eku.md) che rappresenta la proprietà EKU indicizzata. Si tratta della proprietà predefinita.<br/>                                                                                                      |



 

## <a name="remarks"></a>Commenti

Questa raccolta viene recuperata [**dalla proprietà ExtendedKeyUsage.EKUsus.**](extendedkeyusage-ekus.md)

Non **è possibile creare l'oggetto** EKU.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|----------------------------------|----------------------------------------------------------------------------------------|
| Fine del supporto client<br/> | Windows Vista<br/>                                                               |
| Fine del supporto server<br/> | Windows Server 2008<br/>                                                         |
| Componente ridistribuibile<br/>       | CAPICOM 2.0 o versioni successive in Windows Server 2003 e Windows XP<br/>                  |
| DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



 

 
