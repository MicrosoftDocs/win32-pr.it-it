---
description: Rappresenta una raccolta di oggetti firmatari.
ms.assetid: 72e86acd-eb87-4eff-bd4e-327630ebbfc4
title: Oggetto signers
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
ms.openlocfilehash: 75eba0ecb2592bf7efc27ecdd63288179e306651
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106325287"
---
# <a name="signers-object"></a>Oggetto signers

\[L'oggetto **signers** è disponibile per l'uso nei sistemi operativi specificati nella sezione requisiti. Usare invece una raccolta di oggetti CmsSigner. Per ulteriori informazioni, vedere la [**classe CmsSigner**](/dotnet/api/system.security.cryptography.pkcs.cmssigner?view=dotnet-plat-ext-3.1&preserve-view=true) nello spazio dei nomi [**System. Security. Cryptography. Pkcs**](/dotnet/api/system.security.cryptography.pkcs?view=dotnet-plat-ext-3.1&preserve-view=true) .\]

L'oggetto **signers** rappresenta una raccolta di oggetti [**firmatari**](signer.md) .

## <a name="when-to-use"></a>Utilizzo

L'oggetto **signers** viene utilizzato per eseguire le attività seguenti:

-   Recuperare il numero di certificati nella raccolta.
-   Recuperare un oggetto **firmatari** specifico dalla raccolta.
-   Scorrere la raccolta.

## <a name="members"></a>Membri

L'oggetto **signers** dispone di questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

L'oggetto **signers** dispone di queste proprietà.



| Proprietà                                        | Tipo di accesso          | Descrizione                                                                                                                                                                                                                     |
|:------------------------------------------------|:---------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_NewEnum**](signers-newenum.md)<br/> | Sola lettura<br/> | Recupera un'interfaccia [**IEnumVARIANT**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) su un oggetto che può essere utilizzato per enumerare la raccolta. Questa proprietà è nascosta all'interno di Visual Basic Scripting Edition (VBScript).<br/> |
| [**Conteggio**](signers-count.md)<br/>       | Sola lettura<br/> | Numero di oggetti [**firmatari**](signer.md) nella raccolta.<br/>                                                                                                                                                        |
| [**Elemento**](signers-item.md)<br/>         | Sola lettura<br/> | Recupera l'oggetto [**firmatario**](signer.md) che rappresenta il firmatario indicizzato. Si tratta della proprietà predefinita.<br/>                                                                                                      |



 

## <a name="remarks"></a>Commenti

Impossibile creare l'oggetto **firmatari** .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|----------------------------|----------------------------------------------------------------------------------------|
| Componente ridistribuibile<br/> | CAPICOM 2,0 o versioni successive in Windows Server 2003 e Windows XP<br/>                  |
| DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Oggetti Cryptography**](cryptography-objects.md)
</dt> </dl>

 

 
