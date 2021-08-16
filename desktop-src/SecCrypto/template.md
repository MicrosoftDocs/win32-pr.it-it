---
description: Rappresenta il modello di estensione del certificato.
ms.assetid: 1ae9220a-f6b3-47c5-bd08-a36ffd84e1f9
title: Oggetto modello
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Template
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 53c7b06fa4194d0adb4124f3978787f5d1fce0ba88e78ef99dcd6ac162eca2c2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118897322"
---
# <a name="template-object"></a>Oggetto modello

\[**L'oggetto** Modello è disponibile per l'uso nei sistemi operativi specificati nella sezione Requisiti. Usare invece la classe [**X509Extension**](/dotnet/api/system.security.cryptography.x509certificates.x509extension?view=netcore-3.1) nello spazio dei nomi [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) chiamando il costruttore che accetta un OID come parametro e quindi usare l'OID per il modello di certificato per recuperare il modello di estensione del certificato.\]

**L'oggetto** Template rappresenta il modello di estensione del certificato.

## <a name="when-to-use"></a>Utilizzo

**L'oggetto** Template viene usato per eseguire le attività seguenti:

-   Determinare se il modello è contrassegnato come critico o presente.
-   Recuperare [*l'identificatore di*](../secgloss/o-gly.md) oggetto (OID) o il nome del modello.
-   Recuperare la versione secondaria o principale del modello.

## <a name="members"></a>Membri

**L'oggetto** Template ha questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

**L'oggetto** Template ha queste proprietà.



| Proprietà                                                 | Tipo di accesso          | Descrizione                                                                                            |
|:---------------------------------------------------------|:---------------------|:-------------------------------------------------------------------------------------------------------|
| [**IsCritical**](template-iscritical.md)<br/>     | Sola lettura<br/> | Recupera un valore booleano che indica se l'estensione del modello è contrassegnata come critica.<br/> |
| [**IsPresent**](template-ispresent.md)<br/>       | Sola lettura<br/> | Recupera un valore booleano che indica se l'estensione del modello è presente.<br/>         |
| [**Majorversion**](template-majorversion.md)<br/> | Sola lettura<br/> | Recupera il numero di versione principale del modello.<br/>                                         |
| [**Minorversion**](template-minorversion.md)<br/> | Sola lettura<br/> | Recupera il numero di versione secondaria del modello.<br/>                                         |
| [**Nome**](template-name.md)<br/>                 | Sola lettura<br/> | Recupera una stringa contenente il nome del modello.<br/>                                  |
| [**Oid**](template-oid.md)<br/>                   | Sola lettura<br/> | Recupera un [**oggetto OID**](oid.md) che identifica l'oggetto Template. <br/>             |



 

## <a name="remarks"></a>Commenti

Impossibile **creare** l'oggetto Modello.

Un **oggetto Template** viene restituito dal metodo [**Certificate.Template.**](certificate-template.md)

CAPICOM usa due versioni diverse dei modelli di certificato. La tabella seguente mostra il nome e l'OID per ogni versione del modello di certificato.



| Versione | Nome                               | OID                    |
|---------|------------------------------------|------------------------|
| V1      | SzOID \_ ENROLL \_ CERTTYPE \_ EXTENSION | "1.3.6.1.4.1.311.20.2" |
| V2      | szOID \_ CERTIFICATE \_ TEMPLATE       | "1.3.6.1.4.1.311.21.7" |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|----------------------------|----------------------------------------------------------------------------------------|
| Componente ridistribuibile<br/> | CAPICOM 2.0 o versioni successive in Windows Server 2003 e Windows XP<br/>                  |
| DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



 

 
