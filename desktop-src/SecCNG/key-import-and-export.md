---
description: È possibile importare ed esportare chiavi simmetriche e chiavi asimmetriche con CNG. È anche possibile usare le funzionalità di esportazione e importazione delle chiavi per spostare le chiavi tra computer.
ms.assetid: 37bda1e0-5dd2-455c-9627-4e7e1b0e04d3
title: Importazione ed esportazione di chiavi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0a4b6c26069911d771697bf06f7464aa14ab7f099e4a0e06991d2fd992efa44a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118907702"
---
# <a name="key-import-and-export"></a>Importazione ed esportazione di chiavi

È possibile importare ed esportare [*chiavi simmetriche*](/windows/desktop/SecGloss/s-gly) e chiavi asimmetriche con CNG. È anche possibile usare le funzionalità di esportazione e importazione delle chiavi per spostare le chiavi tra computer.

## <a name="symmetric-keys"></a>Chiavi simmetriche

Per importare o esportare chiavi simmetriche (o di sessione) in cui viene usata la stessa chiave per crittografare e decrittografare alcuni dati, è possibile usare le funzioni [**BCryptImportKey**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptimportkey) e [**BCryptExportKey.**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptexportkey) In genere, si esporta prima di tutto una chiave usando la **funzione BCryptExportKey** prima di eseguire l'importazione usando **la funzione BCryptImportKey.** Le funzioni sono progettate per abilitare la crittografia delle chiavi esportate e importate usando i parametri *hExportKey* *e hImportKey.* Tuttavia, l'implementazione Microsoft di queste funzioni non supporta la crittografia delle chiavi esportate e importate.

## <a name="asymmetric-keys"></a>Chiavi asimmetriche

Per importare coppie di chiavi asimmetriche (o [*pubbliche/private)*](/windows/desktop/SecGloss/p-gly)in cui una chiave viene usata per crittografare e l'altra viene usata per decrittografare alcuni dati, è possibile usare una delle funzioni [**BCryptImportKeyPair**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptimportkeypair) o [**NCryptImportKey.**](/windows/desktop/api/Ncrypt/nf-ncrypt-ncryptimportkey) Un provider CNG deve codificare la coppia di chiavi usando un tipo [*BLOB di chiave*](/windows/desktop/SecGloss/k-gly) supportato. [**BCryptExportKey**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptexportkey) può essere usato per creare il BLOB della chiave codificata. [Strutture CNG descrive](cng-structures.md) i tipi e le strutture BLOB chiave supportati da Microsoft Key Archiviazione Provider.

Perché [**BCryptExportKey crei**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptexportkey) una coppia di chiavi persistente, il BLOB della chiave di input deve contenere [*una chiave privata*](/windows/desktop/SecGloss/p-gly). [*Le chiavi pubbliche*](/windows/desktop/SecGloss/p-gly) non sono persistenti.

Il nome della chiave e i criteri di esportazione non fanno parte della [*struttura BLOB*](/windows/desktop/SecGloss/b-gly) definita nelle [strutture CNG.](cng-structures.md) Tuttavia, se un BLOB è di un tipo BLOB opaco ,ad esempio l'immagine di memoria di uno stato di chiave interna, il BLOB potrebbe contenere il nome della chiave e le proprietà dei criteri di esportazione.

Nella procedura seguente viene descritto come importare una chiave privata persistente con le relative proprietà.

**Per importare una chiave persistente**

1.  Creare una chiave persistente usando la [**funzione NCryptCreatePersistedKey.**](/windows/desktop/api/Ncrypt/nf-ncrypt-ncryptcreatepersistedkey)
2.  Impostare le proprietà desiderate sull'oggetto chiave usando la [**funzione NCryptSetProperty.**](/windows/desktop/api/Ncrypt/nf-ncrypt-ncryptsetproperty)
3.  Impostare il BLOB della chiave di importazione come proprietà per la chiave, con il tipo BLOB come nome della proprietà.
4.  Finalizzare l'importazione della chiave persistente usando [**la funzione NCryptFinalizeKey.**](/windows/desktop/api/Ncrypt/nf-ncrypt-ncryptfinalizekey)

 

 
