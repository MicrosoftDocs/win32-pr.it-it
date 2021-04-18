---
description: Rappresenta una raccolta di oggetti OID.
ms.assetid: 2c4ff87a-58e1-46aa-9680-29062b05308c
title: Oggetto Oid
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
ms.openlocfilehash: 894689c214d8b7d352a2453d2d62c847866b9bc5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106325152"
---
# <a name="oids-object"></a>Oggetto Oid

\[L'oggetto **OID** è disponibile per l'uso nei sistemi operativi specificati nella sezione requisiti. Usare invece la [**classe OidCollection**](/dotnet/api/system.security.cryptography.oidcollection?view=netcore-3.1) nello spazio dei nomi [**System. Security. Cryptography**](/dotnet/api/system.security.cryptography?view=dotnet-plat-ext-3.1&preserve-view=true) .\]

L'oggetto **OID** rappresenta una raccolta di oggetti [**OID**](oid.md) . Ogni oggetto [**OID**](oid.md) rappresenta un identificatore di oggetto singolo.

## <a name="when-to-use"></a>Utilizzo

L'oggetto **OID** viene usato per eseguire le attività seguenti:

-   Aggiungere o rimuovere un oggetto [**OID**](oid.md) dalla raccolta.
-   Cancellare tutti gli oggetti [**OID**](oid.md) dalla raccolta.
-   Recuperare il numero di identificatori di oggetto nella raccolta.
-   Recuperare un oggetto [**OID**](oid.md) specifico dalla raccolta.
-   Scorrere la raccolta.

## <a name="members"></a>Membri

L'oggetto **OID** dispone di questi tipi di membri:

-   [Metodi](#methods)
-   [Proprietà](#properties)

### <a name="methods"></a>Metodi

L'oggetto **OID** dispone di questi metodi.



| Metodo                        | Descrizione                                                                  |
|:------------------------------|:-----------------------------------------------------------------------------|
| [**Aggiungere**](oids-add.md)       | Aggiunge un oggetto [**OID**](oid.md) alla raccolta.<br/>              |
| [**Deselezionare**](oids-clear.md)   | Cancella tutti gli oggetti [**OID**](oid.md) dalla raccolta.<br/>        |
| [**Rimuovi**](oids-remove.md) | Rimuove un oggetto [**OID**](oid.md) indicizzato dalla raccolta.<br/> |



 

### <a name="properties"></a>Proprietà

L'oggetto **OID** dispone di queste proprietà.



| Proprietà                                     | Tipo di accesso          | Descrizione                                                                                                                                                                                                                     |
|:---------------------------------------------|:---------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_NewEnum**](oids-newenum.md)<br/> | Sola lettura<br/> | Recupera un'interfaccia [**IEnumVARIANT**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) su un oggetto che può essere utilizzato per enumerare la raccolta. Questa proprietà è nascosta all'interno di Visual Basic Scripting Edition (VBScript).<br/> |
| [**Conteggio**](oids-count.md)<br/>       | Sola lettura<br/> | Recupera il numero di oggetti [**OID**](oid.md) nella raccolta.<br/>                                                                                                                                                |
| [**Elemento**](oids-item.md)<br/>         | Sola lettura<br/> | Recupera un oggetto [**OID**](oid.md) indicizzato dalla raccolta. Si tratta della proprietà predefinita.<br/>                                                                                                                    |



 

## <a name="remarks"></a>Commenti

Impossibile creare l'oggetto **OID** .

L'oggetto **OID** viene usato dalle proprietà seguenti:

-   [**CertificateStatus. ApplicationPolicies**](certificatestatus-applicationpolicies.md)
-   [**CertificateStatus. CertificatePolicies**](certificatestatus-certificatepolicies.md)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|----------------------------|----------------------------------------------------------------------------------------|
| Componente ridistribuibile<br/> | CAPICOM 2,0 o versioni successive in Windows Server 2003 e Windows XP<br/>                  |
| DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



 

 
