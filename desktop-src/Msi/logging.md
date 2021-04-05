---
description: Questo criterio di sistema per computer viene usato solo se la registrazione non è stata abilitata dall' \# opzione della riga di comando &0034;/l&\# 0034; o da MsiEnableLog.
ms.assetid: d8649808-5dc3-4496-8c2f-da9b1512b5aa
title: Registrazione (Windows Installer)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a461051022791e414fe7e211e4dde33c7e83101b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103756614"
---
# <a name="logging-windows-installer"></a>Registrazione (Windows Installer)

Questo [criterio di sistema](system-policy.md) per computer viene usato solo se la registrazione non è stata abilitata dall'opzione della riga di comando "/l" o da [**MsiEnableLog**](/windows/desktop/api/Msi/nf-msi-msienableloga). Se il criterio è impostato in questo caso, il programma di installazione crea un file di log in% Temp% con il nome casuale: MSI \* . LOG. Specificare la modalità di registrazione impostando il valore dei criteri su una stringa di caratteri. Utilizzare gli stessi caratteri per specificare i criteri della modalità di registrazione utilizzati dall'opzione della [riga di comando](command-line-options.md)"/l". Si noti che non è possibile usare "+" e " \* " per i criteri.

La modalità di registrazione può essere impostata tramite i criteri, un'opzione della riga di comando o a livello di codice. Per ulteriori informazioni su tutti i metodi disponibili per l'impostazione della modalità di registrazione, vedere [registrazione normale](normal-logging.md) nella sezione [registrazione Windows Installer](windows-installer-logging.md) .

È possibile impedire che le informazioni riservate, ad esempio le password, vengano immesse nel file di log e rese visibili. Per ulteriori informazioni, vedere la pagina relativa alla [prevenzione della scrittura di informazioni riservate nel file di log](preventing-confidential-information-from-being-written-into-the-log-file.md)

## <a name="registry-key"></a>Chiave del Registro di sistema

Impostare il valore denominato Logging sotto la chiave del registro di sistema seguente.

**HKEY \_ Criteri software del \_ computer locale** \\  \\  \\ **Microsoft** \\ **Windows** \\ **Installer**

## <a name="data-type"></a>Tipo di dati

**REG \_ SZ**

 

 



