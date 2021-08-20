---
description: Rappresenta un puntatore CPS (Certification Practice Statement) o un qualificatore di avviso utente.
ms.assetid: 857af3d6-aa7b-429a-a056-72573232f72c
title: Oggetto qualificatore
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Qualifier
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 546a4ea5fea67dc386d789f80437fddf7d08c886f9255e6cd09378f2d5bf7e23
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117975727"
---
# <a name="qualifier-object"></a>Oggetto qualificatore

\[**L'oggetto** Qualificatore è disponibile per l'uso nei sistemi operativi specificati nella sezione Requisiti. Usare invece la classe [**X509Extension**](/dotnet/api/system.security.cryptography.x509certificates.x509extension?view=netcore-3.1) nello spazio dei nomi [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) chiamando il costruttore che accetta un OID come parametro e quindi usare l'OID per i criteri certificato per elaborare i qualificatori che fanno parte delle informazioni sui criteri nell'estensione Criteri certificato.\]

**L'oggetto Qualifier** rappresenta un puntatore CPS (Certification Practice Statement) o un qualificatore di avviso utente.

## <a name="when-to-use"></a>Utilizzo

**L'oggetto** Qualifier viene usato per eseguire le attività seguenti:

-   Recuperare l'identificatore di oggetto del qualificatore.
-   Recuperare il Uniform Resource Identifier (URI) che punta a un CPS pubblicato [*dall'autorità di certificazione*](../secgloss/c-gly.md) (CA).
-   Recuperare il nome dell'organizzazione associata al qualificatore.
-   Recuperare il nome e il contenuto di un avviso utente.

## <a name="members"></a>Membri

**L'oggetto Qualifier** ha questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

**L'oggetto Qualifier** ha queste proprietà.



| Proprietà                                                          | Tipo di accesso          | Descrizione                                                                                                                         |
|:------------------------------------------------------------------|:---------------------|:------------------------------------------------------------------------------------------------------------------------------------|
| [**CPSPointer**](qualifier-cpspointer.md)<br/>             | Sola lettura<br/> | Recupera una stringa contenente l'URI che punta a un CPS pubblicato dalla CA.<br/>                                       |
| [**ExplicitText**](qualifier-explicittext.md)<br/>         | Sola lettura<br/> | Recupera una stringa che contiene il contenuto dell'avviso utente. Questa proprietà può essere vuota.<br/>                             |
| [**NoticeNumbers**](qualifier-noticenumbers.md)<br/>       | Sola lettura<br/> | Recupera un oggetto **NoticeNumbers** che contiene la raccolta di numeri di avviso utente. Questa proprietà può essere vuota.<br/>    |
| [**Oid**](qualifier-oid.md)<br/>                           | Sola lettura<br/> | Recupera un [**oggetto OID**](oid.md) che identifica il qualificatore. Si tratta della proprietà predefinita.<br/>                      |
| [**OrganizationName**](qualifier-organizationname.md)<br/> | Sola lettura<br/> | Recupera una stringa contenente il nome dell'organizzazione associata al qualificatore. Questa proprietà può essere vuota.<br/> |



 

## <a name="remarks"></a>Commenti

Impossibile **creare** l'oggetto Qualificatore.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|----------------------------|----------------------------------------------------------------------------------------|
| Componente ridistribuibile<br/> | CAPICOM 2.0 o versioni successive in Windows Server 2003 e Windows XP<br/>                  |
| DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



 

 
