---
description: Rappresenta la chiave privata associata a un certificato.
ms.assetid: 26ad1d1c-17c5-4191-ac97-b911e62b4119
title: Oggetto PrivateKey
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PrivateKey
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: e74720cac1287c08209ce08cabe7b364d385412d94213a83bd114dc46605b7ac
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117977637"
---
# <a name="privatekey-object"></a>Oggetto PrivateKey

\[**L'oggetto PrivateKey** è disponibile per l'uso nei sistemi operativi specificati nella sezione Requisiti. Usare invece la [**proprietà X509Certificate2.PrivateKey**](/dotnet/api/system.security.cryptography.x509certificates.x509certificate2.privatekey?view=netcore-3.1) nello spazio dei nomi [**System.Security.Cryptography.X509Certificates.**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1)\]

**L'oggetto PrivateKey** rappresenta [*la chiave privata*](../secgloss/p-gly.md) associata a un certificato.

## <a name="when-to-use"></a>Utilizzo

**L'oggetto PrivateKey** viene usato per eseguire le attività seguenti:

-   Recuperare informazioni sulla chiave privata.
-   Aprire il contenitore di chiavi private.
-   Eliminare la chiave privata.

## <a name="members"></a>Membri

**L'oggetto PrivateKey** ha questi tipi di membri:

-   [Metodi](#methods)
-   [Proprietà](#properties)

### <a name="methods"></a>Metodi

**L'oggetto PrivateKey** dispone di questi metodi.



| Metodo                                                  | Descrizione                                                                                                                                                          |
|:--------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Elimina**](privatekey-delete.md)                     | Elimina il contenitore di chiavi private a cui fa riferimento **l'oggetto PrivateKey.**<br/>                                                                                |
| [**IsAccessible**](privatekey-isaccessible.md)         | Recupera un valore booleano che indica se la chiave privata è accessibile dall'utente. Se true, l'utente può accedere alla chiave privata.<br/>                 |
| [**IsExportable**](privatekey-isexportable.md)         | Recupera un valore booleano che indica se la chiave privata può essere esportata. Se true, è possibile esportare la chiave privata.<br/>                               |
| [**IsHardwareDevice**](privatekey-ishardwaredevice.md) | Recupera un valore booleano che indica se la chiave privata è archiviata in un dispositivo hardware. Se true, la chiave privata viene archiviata in un dispositivo hardware.<br/> |
| [**IsMachineKeyset**](privatekey-ismachinekeyset.md)   | Recupera un valore booleano che indica se la chiave privata è una chiave del computer. Se true, la chiave privata è una chiave del computer.<br/>                             |
| [**IsProtected**](privatekey-isprotected.md)           | Recupera un valore booleano che indica se la chiave privata è protetta. Se true, la chiave privata è protetta.<br/>                                     |
| [**IsRemovable**](privatekey-isremovable.md)           | Recupera un valore booleano che indica se la chiave privata si trova in un dispositivo rimovibile. Se true, la chiave privata si trova in un dispositivo rimovibile.<br/>             |
| [**Aperto**](privatekey-open.md)                         | Accede a un contenitore di chiavi esistente.<br/>                                                                                                                       |



 

### <a name="properties"></a>Proprietà

**L'oggetto PrivateKey** ha queste proprietà.



| Proprietà                                                                 | Tipo di accesso          | Descrizione                                                                                               |
|:-------------------------------------------------------------------------|:---------------------|:----------------------------------------------------------------------------------------------------------|
| [**Containername**](privatekey-containername.md)<br/>             | Sola lettura<br/> | Recupera una stringa che contiene il nome del contenitore di chiavi private. Si tratta della proprietà predefinita.<br/> |
| [**KeySpec**](privatekey-keyspec.md)<br/>                         | Sola lettura<br/> | Recupera la specifica della chiave.<br/>                                                               |
| [**ProviderName**](privatekey-providername.md)<br/>               | Sola lettura<br/> | Recupera una stringa che contiene il nome del provider di servizi di connessione.<br/>                                          |
| [**ProviderType**](privatekey-providertype.md)<br/>               | Sola lettura<br/> | Recupera un valore di enumerazione che specifica il tipo di provider.<br/>                            |
| [**UniqueContainerName**](privatekey-uniquecontainername.md)<br/> | Sola lettura<br/> | Recupera una stringa che contiene il nome univoco del contenitore di chiavi private.<br/>                        |



 

## <a name="remarks"></a>Commenti

**L'oggetto PrivateKey** può essere creato ed è sicuro per lo scripting. Il ProgID per **l'oggetto PrivateKey** è CAPICOM. PrivateKey.1.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|----------------------------|----------------------------------------------------------------------------------------|
| Componente ridistribuibile<br/> | CAPICOM 2.0 o versioni successive in Windows Server 2003 e Windows XP<br/>                  |
| DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



 

 
