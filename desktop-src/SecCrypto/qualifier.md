---
description: Rappresenta un puntatore CPS (Certification Practice Statement) o un qualificatore di avviso utente.
ms.assetid: 857af3d6-aa7b-429a-a056-72573232f72c
title: Oggetto Qualifier
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
ms.openlocfilehash: 3b1740e064cac53f93d9c81603477a1230c7fd7a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106328595"
---
# <a name="qualifier-object"></a>Oggetto Qualifier

\[L'oggetto **qualificatore** è disponibile per l'uso nei sistemi operativi specificati nella sezione requisiti. Usare invece la [**classe X509Extension**](/dotnet/api/system.security.cryptography.x509certificates.x509extension?view=netcore-3.1) nello spazio dei nomi [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) chiamando il costruttore che accetta un OID come parametro e quindi usare l'OID per i criteri dei certificati per elaborare i qualificatori che fanno parte delle informazioni sui criteri nell'estensione criteri di certificato.\]

L'oggetto **qualificatore** rappresenta un puntatore CPS (Certification Practice Statement) o un qualificatore di avviso utente.

## <a name="when-to-use"></a>Utilizzo

L'oggetto **qualificatore** viene utilizzato per eseguire le attività seguenti:

-   Recuperare l'identificatore di oggetto del qualificatore.
-   Recuperare il Uniform Resource Identifier (URI) che punta a un CPS pubblicato dall' [*autorità di certificazione*](../secgloss/c-gly.md) (CA).
-   Recuperare il nome dell'organizzazione associata al qualificatore.
-   Recuperare il nome e il contenuto di un avviso utente.

## <a name="members"></a>Membri

L'oggetto **qualificatore** presenta questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

L'oggetto **qualificatore** dispone di queste proprietà.



| Proprietà                                                          | Tipo di accesso          | Descrizione                                                                                                                         |
|:------------------------------------------------------------------|:---------------------|:------------------------------------------------------------------------------------------------------------------------------------|
| [**CPSPointer**](qualifier-cpspointer.md)<br/>             | Sola lettura<br/> | Recupera una stringa che contiene l'URI che punta a un CPS pubblicato dalla CA.<br/>                                       |
| [**ExplicitText**](qualifier-explicittext.md)<br/>         | Sola lettura<br/> | Recupera una stringa che contiene il contenuto della comunicazione utente. Questa proprietà può essere vuota.<br/>                             |
| [**NoticeNumbers**](qualifier-noticenumbers.md)<br/>       | Sola lettura<br/> | Recupera un oggetto **NoticeNumbers** che contiene la raccolta di numeri di nota utente. Questa proprietà può essere vuota.<br/>    |
| [**OID**](qualifier-oid.md)<br/>                           | Sola lettura<br/> | Recupera un oggetto [**OID**](oid.md) che identifica il qualificatore. Si tratta della proprietà predefinita.<br/>                      |
| [**OrganizationName**](qualifier-organizationname.md)<br/> | Sola lettura<br/> | Recupera una stringa che contiene il nome dell'organizzazione associata al qualificatore. Questa proprietà può essere vuota.<br/> |



 

## <a name="remarks"></a>Commenti

Impossibile creare l'oggetto **qualificatore** .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|----------------------------|----------------------------------------------------------------------------------------|
| Componente ridistribuibile<br/> | CAPICOM 2,0 o versioni successive in Windows Server 2003 e Windows XP<br/>                  |
| DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



 

 
