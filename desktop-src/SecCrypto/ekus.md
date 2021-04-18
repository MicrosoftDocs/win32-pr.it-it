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
ms.openlocfilehash: 56fd6eaeb5a00549cbb4ee659b99ece391e0ebed
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106331425"
---
# <a name="ekus-object"></a>Oggetto EKU

\[CAPICOM è un componente solo a 32 bit disponibile per l'uso nei sistemi operativi seguenti: Windows Server 2008, Windows Vista e Windows XP. Usare invece la [**classe X509ExtensionCollection**](/dotnet/api/system.security.cryptography.x509certificates.x509extensioncollection?view=netcore-3.1) nello spazio dei nomi [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]

L'oggetto **EKU** rappresenta una raccolta di oggetti [**EKU**](eku.md) . Ogni oggetto [**EKU**](eku.md) rappresenta una singola proprietà di utilizzo chiavi avanzato (EKU) di un certificato.

## <a name="when-to-use"></a>Utilizzo

La raccolta **EKU** viene utilizzata per eseguire le attività seguenti:

-   Recuperare il numero di proprietà EKU nella raccolta.
-   Recuperare un oggetto [**EKU**](eku.md) specifico dalla raccolta.
-   Scorrere la raccolta.

## <a name="members"></a>Membri

L'oggetto **EKU** dispone di questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

L'oggetto **EKU** dispone di queste proprietà.



| Proprietà                                     | Tipo di accesso          | Descrizione                                                                                                                                                                                                                     |
|:---------------------------------------------|:---------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_NewEnum**](ekus-newenum.md)<br/> | Sola lettura<br/> | Recupera un'interfaccia [**IEnumVARIANT**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) su un oggetto che può essere utilizzato per enumerare la raccolta. Questa proprietà è nascosta all'interno di Visual Basic Scripting Edition (VBScript).<br/> |
| [**Conteggio**](ekus-count.md)<br/>       | Sola lettura<br/> | Recupera il numero di oggetti [**EKU**](eku.md) nell'insieme.<br/>                                                                                                                                                |
| [**Elemento**](ekus-item.md)<br/>         | Sola lettura<br/> | Recupera l'oggetto [**EKU**](eku.md) che rappresenta la proprietà EKU indicizzata. Si tratta della proprietà predefinita.<br/>                                                                                                      |



 

## <a name="remarks"></a>Commenti

Questa raccolta viene recuperata dalla proprietà [**ExtendedKeyUsage. EKU**](extendedkeyusage-ekus.md) .

Impossibile creare l'oggetto **EKU** .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|----------------------------------|----------------------------------------------------------------------------------------|
| Fine del supporto client<br/> | Windows Vista<br/>                                                               |
| Fine del supporto server<br/> | Windows Server 2008<br/>                                                         |
| Componente ridistribuibile<br/>       | CAPICOM 2,0 o versioni successive in Windows Server 2003 e Windows XP<br/>                  |
| DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



 

 
