---
description: Rappresenta una raccolta di oggetti Signer.
ms.assetid: 72e86acd-eb87-4eff-bd4e-327630ebbfc4
title: Oggetto Signers
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Signers
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 62c5f59fc90d0d34226b4442b8fa443ad734d474e8077bf210df8bfdf752b1ef
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118898334"
---
# <a name="signers-object"></a>Oggetto Signers

\[**L'oggetto** Firmatari è disponibile per l'uso nei sistemi operativi specificati nella sezione Requisiti. Usare invece una raccolta di oggetti CmsSigner. Per altre informazioni, vedere la [**classe CmsSigner**](/dotnet/api/system.security.cryptography.pkcs.cmssigner?view=dotnet-plat-ext-3.1&preserve-view=true) nello spazio dei nomi [**System.Security.Cryptography.Pkcs.**](/dotnet/api/system.security.cryptography.pkcs?view=dotnet-plat-ext-3.1&preserve-view=true)\]

**L'oggetto Signers** rappresenta una raccolta di [**oggetti Signer.**](signer.md)

## <a name="when-to-use"></a>Utilizzo

**L'oggetto Signers** viene usato per eseguire le attività seguenti:

-   Recuperare il numero di certificati nella raccolta.
-   Recuperare un **oggetto Signers** specifico dalla raccolta.
-   Scorrere la raccolta.

## <a name="members"></a>Membri

**L'oggetto Signers** ha questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

**L'oggetto Signers** ha queste proprietà.



| Proprietà                                        | Tipo di accesso          | Descrizione                                                                                                                                                                                                                     |
|:------------------------------------------------|:---------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_NewEnum**](signers-newenum.md)<br/> | Sola lettura<br/> | Recupera [**un'interfaccia IEnumVARIANT**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) su un oggetto che può essere usato per enumerare la raccolta. Questa proprietà è nascosta all'interno di Visual Basic Scripting Edition (VBScript).<br/> |
| [**Conteggio**](signers-count.md)<br/>       | Sola lettura<br/> | Numero di [**oggetti Signer**](signer.md) nella raccolta.<br/>                                                                                                                                                        |
| [**Elemento**](signers-item.md)<br/>         | Sola lettura<br/> | Recupera [**l'oggetto Signer**](signer.md) che rappresenta il firmatario indicizzato. Si tratta della proprietà predefinita.<br/>                                                                                                      |



 

## <a name="remarks"></a>Commenti

Impossibile **creare l'oggetto** Firmatari.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|----------------------------|----------------------------------------------------------------------------------------|
| Componente ridistribuibile<br/> | CAPICOM 2.0 o versioni successive in Windows Server 2003 e Windows XP<br/>                  |
| DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Oggetti di crittografia**](cryptography-objects.md)
</dt> </dl>

 

 
