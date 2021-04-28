---
description: 'Oggetto Recipients: rappresenta una raccolta di oggetti Certificate.'
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
ms.openlocfilehash: e0f0f6474c6ed8883eb591591eff387fe387f7d6
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108103739"
---
# <a name="recipients-object"></a>Oggetto Recipients

\[**L'oggetto** Recipients è disponibile per l'uso nei sistemi operativi specificati nella sezione Requisiti. Usare invece la [**classe CmsRecipientCollection**](/dotnet/api/system.security.cryptography.pkcs.cmsrecipientcollection?view=dotnet-plat-ext-3.1&preserve-view=true) nello spazio dei nomi [**System.Security.Cryptography.Pkcs.**](/dotnet/api/system.security.cryptography.pkcs?view=dotnet-plat-ext-3.1&preserve-view=true)\]

**L'oggetto Recipients** rappresenta una raccolta di [**oggetti**](certificate.md) Certificate. Ogni oggetto rappresenta un destinatario previsto del messaggio in busta. I dati in un oggetto [**EnvelopedData**](envelopeddata.md) vengono crittografati con una chiave di sessione simmetrica e tale chiave di sessione simmetrica viene quindi crittografata per ogni destinatario usando la chiave pubblica del certificato del destinatario. [](../secgloss/s-gly.md) Un destinatario con accesso alla chiave privata [](../secgloss/p-gly.md) associata alla [](../secgloss/s-gly.md) chiave pubblica di un certificato può decrittografare la chiave di sessione e usare la chiave di sessione decrittografata per decrittografare i dati effettivi. [](../secgloss/p-gly.md)

## <a name="when-to-use"></a>Utilizzo

**L'oggetto Recipients** viene usato per eseguire le attività seguenti:

-   Aggiungere o rimuovere un [**oggetto Certificate**](certificate.md) dalla raccolta.
-   Recuperare il numero di certificati nella raccolta.
-   Recuperare un oggetto **Destinatari** specifico dalla raccolta.
-   Scorrere la raccolta.

## <a name="members"></a>Membri

**L'oggetto Recipients** ha questi tipi di membri:

-   [Metodi](#methods)
-   [Proprietà](#properties)

### <a name="methods"></a>Metodi

**L'oggetto Recipients** dispone di questi metodi.



| Metodo                              | Descrizione                                                                            |
|:------------------------------------|:---------------------------------------------------------------------------------------|
| [**Aggiungere**](recipients-add.md)       | Aggiunge un [**oggetto Certificate**](certificate.md) alla raccolta.<br/>         |
| [**Chiaro**](recipients-clear.md)   | Rimuove tutti [**gli oggetti Certificate**](certificate.md) dalla raccolta.<br/> |
| [**Rimuovi**](recipients-remove.md) | Rimuove un [**oggetto Certificate**](certificate.md) dalla raccolta.<br/>    |



 

### <a name="properties"></a>Proprietà

**L'oggetto Recipients** ha queste proprietà.



| Proprietà                                           | Tipo di accesso          | Descrizione                                                                                                                                                                                                                     |
|:---------------------------------------------------|:---------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_NewEnum**](recipients-newenum.md)<br/> | Sola lettura<br/> | Recupera [**un'interfaccia IEnumVARIANT**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) su un oggetto che può essere utilizzato per enumerare la raccolta. Questa proprietà è nascosta in Visual Basic Scripting Edition (VBScript).<br/> |
| [**Conteggio**](recipients-count.md)<br/>       |                      | Numero di oggetti nella **raccolta Recipients.**<br/>                                                                                                                                                              |
| [**Elemento**](recipients-item.md)<br/>         |                      | Oggetto indicizzato nella raccolta. Si tratta della proprietà predefinita.<br/>                                                                                                                                                   |



 

## <a name="remarks"></a>Commenti

Impossibile **creare l'oggetto** Recipients.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|----------------------------|----------------------------------------------------------------------------------------|
| Componente ridistribuibile<br/> | CAPICOM 2.0 o versioni successive in Windows Server 2003 e Windows XP<br/>                  |
| DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Oggetti di crittografia**](cryptography-objects.md)
</dt> </dl>

 

 
