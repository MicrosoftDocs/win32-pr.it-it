---
description: Rappresenta un identificatore di oggetto (OID) utilizzato da diverse proprietà di CAPICOM.
ms.assetid: d9dc2a9a-920b-41e1-91fb-da1628df577d
title: OID (oggetto)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- OID
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: a524bfd8d2eb2edcf3c97919129dd694414d5ace
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106333563"
---
# <a name="oid-object"></a>OID (oggetto)

\[L'oggetto **OID** è disponibile per l'uso nei sistemi operativi specificati nella sezione requisiti. Usare invece la [**classe Oid**](/dotnet/api/system.security.cryptography.oid?view=netcore-3.1) nello spazio dei nomi [**System. Security. Cryptography**](/dotnet/api/system.security.cryptography?view=dotnet-plat-ext-3.1&preserve-view=true) .\]

L'oggetto **OID** rappresenta un [*identificatore di oggetto*](../secgloss/o-gly.md) (OID) utilizzato da diverse proprietà di CAPICOM.

## <a name="when-to-use"></a>Utilizzo

L'oggetto **OID** viene utilizzato per eseguire le attività seguenti:

-   Impostare o recuperare un nome di CAPICOM e un nome visualizzato per l'OID.
-   Impostare o recuperare il numero tratteggiato per l'OID.

## <a name="members"></a>Membri

L'oggetto **OID** presenta questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

L'oggetto **OID** dispone di queste proprietà.



| Proprietà                                            | Tipo di accesso           | Descrizione                                                                                      |
|:----------------------------------------------------|:----------------------|:-------------------------------------------------------------------------------------------------|
| [**FriendlyName**](oid-friendlyname.md)<br/> | Lettura/Scrittura<br/> | Imposta o Recupera il nome visualizzato per l'OID.<br/>                                       |
| [**Nome**](oid-name.md)<br/>                 | Lettura/Scrittura<br/> | Imposta o Recupera il nome definito da CAPICOM per l'OID. Si tratta della proprietà predefinita.<br/> |
| [**Valore**](oid-value.md)<br/>               | Lettura/Scrittura<br/> | Imposta o Recupera il valore del numero tratteggiato dell'OID.<br/>                      |



 

## <a name="remarks"></a>Commenti

È possibile creare l'oggetto **OID** ed è sicuro per lo scripting. Il ProgID per l'oggetto **OID** è capicom. OID. 1.

Le proprietà dell'oggetto CAPICOM seguenti restituiscono un oggetto **OID** :

-   [**PolicyInformation. OID**](policyinformation-oid.md)
-   [**Qualificatore. OID**](qualifier-oid.md)
-   [**Estensione OID**](extension-oid.md)
-   [**Template. OID**](template-oid.md)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|----------------------------|----------------------------------------------------------------------------------------|
| Componente ridistribuibile<br/> | CAPICOM 2,0 o versioni successive in Windows Server 2003 e Windows XP<br/>                  |
| DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



 

 
