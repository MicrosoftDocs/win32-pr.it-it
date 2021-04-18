---
description: Rappresenta una raccolta di oggetti certificate.
ms.assetid: 11d294b5-0a8a-4970-be10-a3b22389d96e
title: Oggetto Recipients
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Recipients
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: c68ca0217631970f35680160b71841f758b13fd7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106324462"
---
# <a name="recipients-object"></a>Oggetto Recipients

\[L'oggetto **destinatari** è disponibile per l'uso nei sistemi operativi specificati nella sezione requisiti. Usare invece la [**classe CmsRecipientCollection**](/dotnet/api/system.security.cryptography.pkcs.cmsrecipientcollection?view=dotnet-plat-ext-3.1&preserve-view=true) nello spazio dei nomi [**System. Security. Cryptography. Pkcs**](/dotnet/api/system.security.cryptography.pkcs?view=dotnet-plat-ext-3.1&preserve-view=true) .\]

L'oggetto **Recipients** rappresenta una raccolta di oggetti [**Certificate**](certificate.md) . Ogni oggetto rappresenta un destinatario previsto del messaggio in busta digitale. I dati in un oggetto [**EnvelopedData**](envelopeddata.md) vengono crittografati con una chiave di sessione [*simmetrica*](../secgloss/s-gly.md) e la chiave della sessione simmetrica viene quindi crittografata per ogni destinatario utilizzando la chiave pubblica del certificato del destinatario desiderato. Un destinatario con accesso alla [*chiave privata*](../secgloss/p-gly.md) associata alla [*chiave pubblica*](../secgloss/p-gly.md) di un certificato può decrittografare la [*chiave della sessione*](../secgloss/s-gly.md) e utilizzare la chiave della sessione decrittografata per decrittografare i dati effettivi.

## <a name="when-to-use"></a>Utilizzo

L'oggetto **Recipients** viene utilizzato per eseguire le attività seguenti:

-   Aggiungere o rimuovere un oggetto [**certificato**](certificate.md) dalla raccolta.
-   Recuperare il numero di certificati nella raccolta.
-   Recuperare un oggetto **destinatari** specifico dalla raccolta.
-   Scorrere la raccolta.

## <a name="members"></a>Membri

L'oggetto **destinatari** presenta questi tipi di membri:

-   [Metodi](#methods)
-   [Proprietà](#properties)

### <a name="methods"></a>Metodi

L'oggetto **Recipients** dispone di questi metodi.



| Metodo                              | Descrizione                                                                            |
|:------------------------------------|:---------------------------------------------------------------------------------------|
| [**Aggiungere**](recipients-add.md)       | Aggiunge un oggetto [**certificato**](certificate.md) alla raccolta.<br/>         |
| [**Deselezionare**](recipients-clear.md)   | Rimuove tutti gli oggetti [**certificato**](certificate.md) dalla raccolta.<br/> |
| [**Rimuovi**](recipients-remove.md) | Rimuove un oggetto [**certificato**](certificate.md) dalla raccolta.<br/>    |



 

### <a name="properties"></a>Proprietà

L'oggetto **destinatari** dispone di queste proprietà.



| Proprietà                                           | Tipo di accesso          | Descrizione                                                                                                                                                                                                                     |
|:---------------------------------------------------|:---------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_NewEnum**](recipients-newenum.md)<br/> | Sola lettura<br/> | Recupera un'interfaccia [**IEnumVARIANT**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) su un oggetto che può essere utilizzato per enumerare la raccolta. Questa proprietà è nascosta all'interno di Visual Basic Scripting Edition (VBScript).<br/> |
| [**Conteggio**](recipients-count.md)<br/>       |                      | Numero di oggetti nella raccolta di **destinatari** .<br/>                                                                                                                                                              |
| [**Elemento**](recipients-item.md)<br/>         |                      | Oggetto indicizzato nella raccolta. Si tratta della proprietà predefinita.<br/>                                                                                                                                                   |



 

## <a name="remarks"></a>Commenti

Impossibile creare l'oggetto **destinatari** .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|----------------------------|----------------------------------------------------------------------------------------|
| Componente ridistribuibile<br/> | CAPICOM 2,0 o versioni successive in Windows Server 2003 e Windows XP<br/>                  |
| DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Oggetti Cryptography**](cryptography-objects.md)
</dt> </dl>

 

 
