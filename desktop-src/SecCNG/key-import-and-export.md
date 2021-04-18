---
description: È possibile importare ed esportare chiavi simmetriche e chiavi asimmetriche con CNG. È possibile usare le funzionalità principali di esportazione e importazione per spostare le chiavi tra i computer.
ms.assetid: 37bda1e0-5dd2-455c-9627-4e7e1b0e04d3
title: Importazione ed esportazione di chiavi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8be59cc5f5c4b3d1a98fa30cf4e967d5469d2f1f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106305605"
---
# <a name="key-import-and-export"></a>Importazione ed esportazione di chiavi

È possibile importare ed esportare [*chiavi simmetriche*](/windows/desktop/SecGloss/s-gly) e chiavi asimmetriche con CNG. È possibile usare le funzionalità principali di esportazione e importazione per spostare le chiavi tra i computer.

## <a name="symmetric-keys"></a>Chiavi simmetriche

Per importare o esportare chiavi simmetriche (o di sessione) in cui viene usata la stessa chiave per crittografare e decrittografare alcuni dati, è possibile usare le funzioni [**BCryptImportKey**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptimportkey) e [**BCryptExportKey**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptexportkey) . In genere, è necessario innanzitutto esportare una chiave utilizzando la funzione **BCryptExportKey** prima di eseguire l'importazione tramite la funzione **BCryptImportKey** . Le funzioni sono progettate per abilitare la crittografia delle chiavi esportate e importate usando i parametri *hExportKey* e *hImportKey* . Tuttavia, l'implementazione Microsoft di queste funzioni non supporta la crittografia delle chiavi esportate e importate.

## <a name="asymmetric-keys"></a>Chiavi asimmetriche

Per importare coppie di chiavi asimmetriche (o [*pubbliche/private*](/windows/desktop/SecGloss/p-gly)) in cui una chiave viene usata per crittografare e l'altra per decrittografare alcuni dati, è possibile usare una delle funzioni [**BCryptImportKeyPair**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptimportkeypair) o [**NCryptImportKey**](/windows/desktop/api/Ncrypt/nf-ncrypt-ncryptimportkey) . Un provider CNG deve codificare la coppia di chiavi usando un tipo di [*BLOB di chiavi*](/windows/desktop/SecGloss/k-gly) supportato. [**BCryptExportKey**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptexportkey) può essere usato per creare il BLOB di chiavi codificate. Le [strutture CNG](cng-structures.md) descrivono i tipi e le strutture BLOB principali supportati dal provider di archiviazione chiavi Microsoft.

Per [**BCryptExportKey**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptexportkey) creare una coppia di chiavi permanente, il BLOB della chiave di input deve contenere una [*chiave privata*](/windows/desktop/SecGloss/p-gly). Le [*chiavi pubbliche*](/windows/desktop/SecGloss/p-gly) non sono rese permanente.

Il nome della chiave e i criteri di esportazione non fanno parte della struttura [*BLOB*](/windows/desktop/SecGloss/b-gly) definita nelle [strutture CNG](cng-structures.md). Tuttavia, se un BLOB è di un tipo di BLOB opaco, ad esempio l'immagine di memoria di uno stato di chiave interna, il BLOB potrebbe contenere il nome della chiave e le proprietà dei criteri di esportazione.

Nella procedura riportata di seguito viene descritto come importare una chiave privata permanente con le relative proprietà.

**Per importare una chiave salvata in modo permanente**

1.  Creare una chiave permanente usando la funzione [**NCryptCreatePersistedKey**](/windows/desktop/api/Ncrypt/nf-ncrypt-ncryptcreatepersistedkey) .
2.  Impostare le proprietà desiderate nell'oggetto chiave utilizzando la funzione [**NCryptSetProperty**](/windows/desktop/api/Ncrypt/nf-ncrypt-ncryptsetproperty) .
3.  Impostare il BLOB della chiave di importazione come proprietà nella chiave, con il tipo di BLOB come nome della proprietà.
4.  Finalizzare l'importazione della chiave permanente tramite la funzione [**NCryptFinalizeKey**](/windows/desktop/api/Ncrypt/nf-ncrypt-ncryptfinalizekey) .

 

 
