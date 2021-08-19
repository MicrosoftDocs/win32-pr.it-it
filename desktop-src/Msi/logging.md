---
description: Questi criteri di sistema per computer vengono usati solo se la registrazione non è stata abilitata dall'opzione della riga di comando &\# 0034;/L&\# 0034; o da MsiEnableLog.
ms.assetid: d8649808-5dc3-4496-8c2f-da9b1512b5aa
title: Registrazione (Windows di installazione)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e49993419b03e3c092fdf4d2b6d9d118ca4dc2d3d641c82c4fc829cbfd6b68c3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118945636"
---
# <a name="logging-windows-installer"></a>Registrazione (Windows di installazione)

Questo criterio di [sistema](system-policy.md) per computer viene usato solo se la registrazione non è stata abilitata dall'opzione della riga di comando "/L" o da [**MsiEnableLog**](/windows/desktop/api/Msi/nf-msi-msienableloga). Se i criteri sono impostati in questo caso, il programma di installazione crea un file di log in %temp% con il nome casuale: MSI \* . Registro. Specificare la modalità di registrazione impostando il valore del criterio su una stringa di caratteri. Usare gli stessi caratteri per specificare i criteri della modalità di registrazione usati dall'opzione della riga di comando ["/L".](command-line-options.md) Si noti che non è possibile usare "+" \* e " " per i criteri.

La modalità di registrazione può essere impostata tramite criteri, un'opzione della riga di comando o a livello di codice. Per altre informazioni su tutti i metodi disponibili per l'impostazione della modalità di registrazione, vedere [Registrazione](normal-logging.md) normale nella Windows [registrazione del](windows-installer-logging.md) programma di installazione.

È possibile impedire che le informazioni riservate, ad esempio le password, vengano immesse nel file di log e rese visibili. Per altre informazioni, vedere Impedire la scrittura di informazioni riservate [nel file di log](preventing-confidential-information-from-being-written-into-the-log-file.md)

## <a name="registry-key"></a>Chiave del Registro di sistema

Impostare il valore denominato Logging nella chiave del Registro di sistema seguente.

**HKEY \_ Criteri \_ software del computer** \\  \\ **locale** \\ **Microsoft** \\ **Windows** \\ **Installer**

## <a name="data-type"></a>Tipo di dati

**REG \_ SZ**

 

 



