---
description: Fornisce proprietà e metodi che è possibile utilizzare per scegliere, gestire e utilizzare gli archivi certificati e i certificati in tali archivi.
ms.assetid: de4eecf7-c03b-4733-ac29-d5b26b873dba
title: Archiviare un oggetto
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Store
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 1de500d10d6bd5493492b62a2abb618be3cdb19d48a89beaf7ab83d55a86ac28
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117972298"
---
# <a name="store-object"></a>Archiviare un oggetto

\[**L'oggetto** Store è disponibile per l'uso nei sistemi operativi specificati nella sezione Requisiti. Usare invece la [**classe X509Store**](/dotnet/api/system.security.cryptography.x509certificates.x509store?view=netcore-3.1) nello spazio dei [**nomi System.Security.Cryptography.X509Certificates.**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1)\]

**L'oggetto** Store fornisce proprietà e metodi che è possibile usare per scegliere, gestire e usare gli archivi [*certificati*](../secgloss/c-gly.md) e i certificati in tali archivi. CAPICOM può usare gli archivi Current-User, Local-Machine, memory e Active Directory. Inoltre, gli archivi supportano smart card di certificati basati su certificati basati su . Gli sviluppatori devono tenere presente che alcuni metodi potrebbero non riuscire con alcuni archivi se si tenta di eseguire operazioni per le quali l'utente non dispone dei diritti.

## <a name="members"></a>Membri

**L'oggetto Store** ha questi tipi di membri:

-   [Metodi](#methods)
-   [Proprietà](#properties)

### <a name="methods"></a>Metodi

**L'oggetto Store** dispone di questi metodi.



| Metodo                         | Descrizione                                                                                                                                                                                                      |
|:-------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Aggiungere**](store-add.md)       | Aggiunge un [**oggetto Certificato**](certificate.md) all'archivio certificati aperto.<br/>                                                                                                                       |
| [**Chiudi**](store-close.md)   | Chiude un archivio certificati aperto.<br/> **CAPICOM 2.0.0.3 e versioni precedenti:** Il [**metodo Close**](store-close.md) non è supportato.<br/>                                                               |
| [**Elimina**](store-delete.md) | Elimina l'archivio certificati rappresentato dall'oggetto [**Store**](certificate.md) corrente.<br/> **CAPICOM 2.0.0.3 e versioni precedenti:** Il [**metodo Delete**](store-delete.md) non è supportato.<br/> |
| [**Esportazione**](store-export.md) | Esporta l'archivio di un OGGETTO [*BLOB codificato.*](../secgloss/b-gly.md)<br/>                                                                                                       |
| [**Importa**](store-import.md) | Importa un archivio esportato in precedenza.<br/>                                                                                                                                                                  |
| [**Caricamento**](store-load.md)     | Importa [**gli oggetti**](certificate.md) Certificato da un file nell'archivio.<br/>                                                                                                                        |
| [**Aperto**](store-open.md)     | Apre un archivio certificati.<br/>                                                                                                                                                                            |
| [**Rimuovi**](store-remove.md) | Rimuove un [**oggetto Certificato**](certificate.md) da un archivio aperto.<br/>                                                                                                                               |



 

### <a name="properties"></a>Proprietà

**L'oggetto Store** ha queste proprietà.



| Proprietà                                              | Tipo di accesso          | Descrizione                                                                                                                                                                                           |
|:------------------------------------------------------|:---------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Certificati**](store-certificates.md)<br/> | Sola lettura<br/> | Recupera la raccolta [**Certificates**](certificates.md) dell'archivio. Questa è la proprietà predefinita.<br/>                                                                                  |
| [**Località**](store-location.md)<br/>         | Sola lettura<br/> | Recupera il percorso dell'archivio certificati rappresentato da questo oggetto .<br/> **CAPICOM 2.0.0.3 e versioni precedenti:** La [**proprietà Location**](store-location.md) non è supportata.<br/> |
| [**Nome**](store-name.md)<br/>                 | Sola lettura<br/> | Recupera il nome dell'archivio certificati rappresentato da questo oggetto .<br/> **CAPICOM 2.0.0.3 e versioni precedenti:** La [**proprietà Name**](store-name.md) non è supportata.<br/>             |



 

## <a name="remarks"></a>Commenti

**L'oggetto Store** può essere creato ed è sicuro per lo scripting. Il ProgID per **l'oggetto Store** è CAPICOM. Store.2.

**CAPICOM 1. *x*:** il ProgID per l'oggetto **Store** è CAPICOM. Store.1.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|----------------------------|----------------------------------------------------------------------------------------|
| Componente ridistribuibile<br/> | CAPICOM 2.0 o versioni successive in Windows Server 2003 e Windows XP<br/>                  |
| DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Oggetti di crittografia**](cryptography-objects.md)
</dt> </dl>

 

 
