---
description: Fornisce le proprietà e i metodi che è possibile usare per scegliere, gestire e usare gli archivi certificati e i certificati in tali archivi.
ms.assetid: de4eecf7-c03b-4733-ac29-d5b26b873dba
title: Oggetto Store
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
ms.openlocfilehash: 4e8a14fcecf0ded2e4e1a56e2b98e4ac4838b776
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106330019"
---
# <a name="store-object"></a>Oggetto Store

\[L'oggetto **Store** è disponibile per l'uso nei sistemi operativi specificati nella sezione requisiti. Usare invece la [**classe X509Store**](/dotnet/api/system.security.cryptography.x509certificates.x509store?view=netcore-3.1) nello spazio dei nomi [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]

L'oggetto **Store** fornisce le proprietà e i metodi che è possibile usare per scegliere, gestire e usare gli [*archivi certificati*](../secgloss/c-gly.md) e i certificati in tali archivi. CAPICOM può usare gli archivi utente corrente, computer locale, memoria e Active Directory. Inoltre, gli archivi supportano gli archivi certificati basati su smart card. Gli sviluppatori devono tenere presente che alcuni metodi potrebbero avere esito negativo con alcuni archivi se si tenta di eseguire operazioni per le quali l'utente non dispone di diritti.

## <a name="members"></a>Membri

L'oggetto **Store** presenta questi tipi di membri:

-   [Metodi](#methods)
-   [Proprietà](#properties)

### <a name="methods"></a>Metodi

L'oggetto **Store** ha questi metodi.



| Metodo                         | Descrizione                                                                                                                                                                                                      |
|:-------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Aggiungere**](store-add.md)       | Aggiunge un oggetto [**certificato**](certificate.md) all'archivio certificati aperto.<br/>                                                                                                                       |
| [**Chiudi**](store-close.md)   | Chiude un archivio certificati aperto.<br/> **CAPICOM 2.0.0.3 e versioni precedenti:** Il metodo [**Close**](store-close.md) non è supportato.<br/>                                                               |
| [**Delete**](store-delete.md) | Elimina l'archivio certificati rappresentato dall'oggetto [**Archivio**](certificate.md) corrente.<br/> **CAPICOM 2.0.0.3 e versioni precedenti:** Il metodo [**Delete**](store-delete.md) non è supportato.<br/> |
| [**Esportazione**](store-export.md) | Esporta l'archivio di un [*BLOB*](../secgloss/b-gly.md)codificato.<br/>                                                                                                       |
| [**Importa**](store-import.md) | Importa un archivio precedentemente esportato.<br/>                                                                                                                                                                  |
| [**Caricamento**](store-load.md)     | Importa oggetti [**certificato**](certificate.md) da un file nell'archivio.<br/>                                                                                                                        |
| [**Aprire**](store-open.md)     | Apre un archivio certificati.<br/>                                                                                                                                                                            |
| [**Rimuovi**](store-remove.md) | Rimuove un oggetto [**certificato**](certificate.md) da un archivio aperto.<br/>                                                                                                                               |



 

### <a name="properties"></a>Proprietà

L'oggetto **Store** presenta queste proprietà.



| Proprietà                                              | Tipo di accesso          | Descrizione                                                                                                                                                                                           |
|:------------------------------------------------------|:---------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Certificati**](store-certificates.md)<br/> | Sola lettura<br/> | Recupera la raccolta di [**certificati**](certificates.md) dell'archivio. Si tratta della proprietà predefinita.<br/>                                                                                  |
| [**Location**](store-location.md)<br/>         | Sola lettura<br/> | Recupera il percorso dell'archivio certificati rappresentato da questo oggetto.<br/> **CAPICOM 2.0.0.3 e versioni precedenti:** La proprietà [**location**](store-location.md) non è supportata.<br/> |
| [**Nome**](store-name.md)<br/>                 | Sola lettura<br/> | Recupera il nome dell'archivio certificati rappresentato da questo oggetto.<br/> **CAPICOM 2.0.0.3 e versioni precedenti:** La proprietà [**Name**](store-name.md) non è supportata.<br/>             |



 

## <a name="remarks"></a>Commenti

È possibile creare l'oggetto **Store** ed è sicuro per lo scripting. Il ProgID per l'oggetto **Store** è capicom. Archivio. 2.

**CAPICOM 1. *x*:** il ProgID per l'oggetto **Store** è capicom. Archivio. 1.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|----------------------------|----------------------------------------------------------------------------------------|
| Componente ridistribuibile<br/> | CAPICOM 2,0 o versioni successive in Windows Server 2003 e Windows XP<br/>                  |
| DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Oggetti Cryptography**](cryptography-objects.md)
</dt> </dl>

 

 
