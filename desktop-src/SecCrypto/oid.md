---
description: Rappresenta un identificatore di oggetto (OID) utilizzato da diverse proprietà CAPICOM.
ms.assetid: d9dc2a9a-920b-41e1-91fb-da1628df577d
title: Oggetto OID
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
ms.openlocfilehash: a0c37fc1e85dd4d372219e142ed587f9766f9634911afa59b49ce5538023af4c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117979679"
---
# <a name="oid-object"></a>Oggetto OID

\[**L'oggetto OID** è disponibile per l'uso nei sistemi operativi specificati nella sezione Requisiti. Usare invece la [**classe Oid nello**](/dotnet/api/system.security.cryptography.oid?view=netcore-3.1) spazio [**dei nomi System.Security.Cryptography.**](/dotnet/api/system.security.cryptography?view=dotnet-plat-ext-3.1&preserve-view=true)\]

**L'oggetto OID** rappresenta [*un*](../secgloss/o-gly.md) identificatore di oggetto (OID) usato da diverse proprietà CAPICOM.

## <a name="when-to-use"></a>Utilizzo

**L'oggetto OID** viene usato per eseguire le attività seguenti:

-   Impostare o recuperare un nome CAPICOM e un nome visualizzato per l'OID.
-   Impostare o recuperare il numero punteggiato per l'OID.

## <a name="members"></a>Membri

**L'oggetto OID** ha questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

**L'oggetto OID** ha queste proprietà.



| Proprietà                                            | Tipo di accesso           | Descrizione                                                                                      |
|:----------------------------------------------------|:----------------------|:-------------------------------------------------------------------------------------------------|
| [**FriendlyName**](oid-friendlyname.md)<br/> | Lettura/Scrittura<br/> | Imposta o recupera il nome visualizzato per l'OID.<br/>                                       |
| [**Nome**](oid-name.md)<br/>                 | Lettura/Scrittura<br/> | Imposta o recupera il nome definito da CAPICOM per l'OID. Si tratta della proprietà predefinita.<br/> |
| [**Valore**](oid-value.md)<br/>               | Lettura/Scrittura<br/> | Imposta o recupera il valore del numero OID punteggiato dell'OID.<br/>                      |



 

## <a name="remarks"></a>Commenti

**L'oggetto OID** può essere creato ed è sicuro per lo scripting. Il ProgID per **l'oggetto OID** è CAPICOM. OID.1.

Le proprietà dell'oggetto CAPICOM seguenti restituiscono un **oggetto OID:**

-   [**PolicyInformation.OID**](policyinformation-oid.md)
-   [**Qualifier.OID**](qualifier-oid.md)
-   [**Extension.OID**](extension-oid.md)
-   [**Template.OID**](template-oid.md)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|----------------------------|----------------------------------------------------------------------------------------|
| Componente ridistribuibile<br/> | CAPICOM 2.0 o versioni successive in Windows Server 2003 e Windows XP<br/>                  |
| DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



 

 
