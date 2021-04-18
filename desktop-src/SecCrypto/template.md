---
description: Rappresenta il modello di estensione del certificato del certificato.
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
ms.openlocfilehash: fedd64979ad74ceac3f6d54af58c57d8d8b2b134
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106330596"
---
# <a name="template-object"></a>Oggetto modello

\[L'oggetto **modello** è disponibile per l'uso nei sistemi operativi specificati nella sezione requisiti. Usare invece la [**classe X509Extension**](/dotnet/api/system.security.cryptography.x509certificates.x509extension?view=netcore-3.1) nello spazio dei nomi [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) chiamando il costruttore che accetta un OID come parametro e quindi usare OID per il modello di certificato per recuperare il modello di estensione del certificato.\]

L'oggetto **modello** rappresenta il modello di estensione del certificato del certificato.

## <a name="when-to-use"></a>Utilizzo

L'oggetto **modello** viene utilizzato per eseguire le attività seguenti:

-   Determinare se il modello è contrassegnato come critico o presente.
-   Recuperare l' [*identificatore di oggetto*](../secgloss/o-gly.md) (OID) o il nome del modello.
-   Recuperare la versione secondaria o principale del modello.

## <a name="members"></a>Membri

L'oggetto **modello** dispone di questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

L'oggetto **modello** dispone di queste proprietà.



| Proprietà                                                 | Tipo di accesso          | Descrizione                                                                                            |
|:---------------------------------------------------------|:---------------------|:-------------------------------------------------------------------------------------------------------|
| [**IsCritical**](template-iscritical.md)<br/>     | Sola lettura<br/> | Recupera un valore booleano che indica se l'estensione del modello è contrassegnata come critica.<br/> |
| [**IsPresent**](template-ispresent.md)<br/>       | Sola lettura<br/> | Recupera un valore booleano che indica se l'estensione del modello è presente.<br/>         |
| [**MajorVersion**](template-majorversion.md)<br/> | Sola lettura<br/> | Recupera il numero di versione principale del modello.<br/>                                         |
| [**MinorVersion**](template-minorversion.md)<br/> | Sola lettura<br/> | Recupera il numero di versione secondario del modello.<br/>                                         |
| [**Nome**](template-name.md)<br/>                 | Sola lettura<br/> | Recupera una stringa che contiene il nome del modello.<br/>                                  |
| [**OID**](template-oid.md)<br/>                   | Sola lettura<br/> | Recupera un oggetto [**OID**](oid.md) che identifica l'oggetto **modello** .<br/>             |



 

## <a name="remarks"></a>Commenti

Impossibile creare l'oggetto **modello** .

Un oggetto **modello** viene restituito dal metodo [**Certificate. template**](certificate-template.md) .

CAPICOM usa due versioni diverse dei modelli di certificato. La tabella seguente mostra il nome e l'OID per ogni versione del modello di certificato.



| Versione | Nome                               | OID                    |
|---------|------------------------------------|------------------------|
| V1      | szOID \_ registrazione \_ \_ estensione tipo certificato | "1.3.6.1.4.1.311.20.2" |
| V2      | \_modello di certificato szOID \_       | "1.3.6.1.4.1.311.21.7" |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|----------------------------|----------------------------------------------------------------------------------------|
| Componente ridistribuibile<br/> | CAPICOM 2,0 o versioni successive in Windows Server 2003 e Windows XP<br/>                  |
| DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



 

 
