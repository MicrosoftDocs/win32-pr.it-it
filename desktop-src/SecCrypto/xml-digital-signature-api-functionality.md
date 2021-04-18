---
description: CryptXML fornisce un set di API di basso livello che consentono alle applicazioni di creare e verificare le firme, l'inviluppo e lo scollegamento. È possibile usare CryptXML per creare e verificare il contenuto archiviato negli elementi dell'oggetto Signature, inclusi i manifesti.
ms.assetid: 962dffdb-caa6-4aa7-b5c6-3a9de8cfaf6c
title: Funzionalità API firma digitale XML
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 67ae330fdd8ba75ece885e8ed0b7e2c91e60fc39
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106312778"
---
# <a name="xml-digital-signature-api-functionality"></a>Funzionalità API firma digitale XML

CryptXML fornisce un set di API di basso livello che consentono alle applicazioni di creare e verificare le firme, l'inviluppo e lo scollegamento. È possibile usare CryptXML per creare e verificare il contenuto archiviato negli elementi dell'oggetto Signature, inclusi i manifesti. Per firmare e verificare la [*firma digitale*](../secgloss/d-gly.md)XML, è possibile usare una chiave pubblica/privata, una chiave condivisa o un certificato [*X. 509*](../secgloss/x-gly.md) o una catena di certificati.

Le applicazioni che utilizzano CryptXML per verificare i riferimenti esterni (riferimenti destinati a un documento esterno o a un file esterno al contesto del documento) devono risolvere gli URI esterni e recuperare i dati da digerire.

Per informazioni sugli algoritmi di crittografia supportati da CryptXML, vedere algoritmi di [crittografia della firma digitale XML](xml-digital-signature-cryptographic-algorithms.md).

CryptXML fornisce il supporto per gli algoritmi di canonizzazione con i seguenti identificatori.



| Costante                                              | Valore URI                                                                  |
|-------------------------------------------------------|----------------------------------------------------------------------------|
| wszURI \_ canonizzazione \_ c14n<br/>             | "https://www.w3.org/TR/2001/REC-xml-c14n-20010315"<br/>               |
| wszURI \_ canonizzazione \_ C14NC<br/>            | "https://www.w3.org/TR/2001/REC-xml-c14n-20010315\#WithComments"<br/> |
| wszURI \_ canonizzazione \_ EXSLUSIVE \_ c14n<br/>  | "https://www.w3.org/2001/10/xml-exc-c14n\#"<br/>                      |
| wszURI \_ canonizzazione \_ EXSLUSIVE \_ C14NC<br/> | "https://www.w3.org/2001/10/xml-exc-c14n\#WithComments"<br/>          |



 

CryptXML fornisce il supporto per la trasformazione firma protetta.



| Costante                                       | Valore URI                                                           |
|------------------------------------------------|---------------------------------------------------------------------|
| \_trasformazione xmlns wszURI in \_ \_ busta<br/> | "https://www.w3.org/2000/09/xmldsig\#enveloped-signature"<br/> |



 

Per impostazione predefinita, CryptXML non supporta le trasformazioni XPath o XSLT. Se necessario, le applicazioni possono implementare queste trasformazioni in CryptXML.

 

 
