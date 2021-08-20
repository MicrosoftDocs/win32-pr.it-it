---
description: Rappresenta una raccolta di oggetti OID.
ms.assetid: 2c4ff87a-58e1-46aa-9680-29062b05308c
title: Oggetto OID
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- OIDs
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 32b6e2847a3e9848a67f0b96724e8883e2857d63abbaecc0a071f1a03eb03d2a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117979183"
---
# <a name="oids-object"></a>Oggetto OID

\[**L'oggetto OID** è disponibile per l'uso nei sistemi operativi specificati nella sezione Requisiti. Usare invece la [**classe OidCollection nello**](/dotnet/api/system.security.cryptography.oidcollection?view=netcore-3.1) spazio [**dei nomi System.Security.Cryptography.**](/dotnet/api/system.security.cryptography?view=dotnet-plat-ext-3.1&preserve-view=true)\]

**L'oggetto OID** rappresenta una raccolta di [**oggetti OID.**](oid.md) Ogni [**oggetto OID**](oid.md) rappresenta un singolo identificatore di oggetto.

## <a name="when-to-use"></a>Utilizzo

**L'oggetto OID** viene usato per eseguire le attività seguenti:

-   Aggiungere o rimuovere un [**oggetto OID**](oid.md) dalla raccolta.
-   Cancellare tutti gli [**oggetti OID**](oid.md) dalla raccolta.
-   Recuperare il numero di identificatori di oggetto nella raccolta.
-   Recuperare un [**oggetto OID**](oid.md) specifico dalla raccolta.
-   Scorrere la raccolta.

## <a name="members"></a>Membri

**L'oggetto OID** ha questi tipi di membri:

-   [Metodi](#methods)
-   [Proprietà](#properties)

### <a name="methods"></a>Metodi

**L'oggetto OID** dispone di questi metodi.



| Metodo                        | Descrizione                                                                  |
|:------------------------------|:-----------------------------------------------------------------------------|
| [**Aggiungere**](oids-add.md)       | Aggiunge un [**oggetto OID**](oid.md) alla raccolta.<br/>              |
| [**Cancella**](oids-clear.md)   | Cancella tutti [**gli oggetti OID**](oid.md) dalla raccolta.<br/>        |
| [**Rimuovi**](oids-remove.md) | Rimuove un [**oggetto OID indicizzato**](oid.md) dalla raccolta.<br/> |



 

### <a name="properties"></a>Proprietà

**L'oggetto OID** ha queste proprietà.



| Proprietà                                     | Tipo di accesso          | Descrizione                                                                                                                                                                                                                     |
|:---------------------------------------------|:---------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_NewEnum**](oids-newenum.md)<br/> | Sola lettura<br/> | Recupera [**un'interfaccia IEnumVARIANT**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) su un oggetto che può essere usato per enumerare la raccolta. Questa proprietà è nascosta in Visual Basic Scripting Edition (VBScript).<br/> |
| [**Conteggio**](oids-count.md)<br/>       | Sola lettura<br/> | Recupera il numero di [**oggetti OID**](oid.md) nella raccolta.<br/>                                                                                                                                                |
| [**Elemento**](oids-item.md)<br/>         | Sola lettura<br/> | Recupera un oggetto [**OID indicizzato**](oid.md) dalla raccolta. Si tratta della proprietà predefinita.<br/>                                                                                                                    |



 

## <a name="remarks"></a>Commenti

Impossibile **creare l'oggetto OID.**

**L'oggetto OIDs** viene usato dalle proprietà seguenti:

-   [**CertificateStatus.ApplicationPolicies**](certificatestatus-applicationpolicies.md)
-   [**CertificateStatus.CertificatePolicies**](certificatestatus-certificatepolicies.md)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|----------------------------|----------------------------------------------------------------------------------------|
| Componente ridistribuibile<br/> | CAPICOM 2.0 o versioni successive in Windows Server 2003 e Windows XP<br/>                  |
| DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



 

 
