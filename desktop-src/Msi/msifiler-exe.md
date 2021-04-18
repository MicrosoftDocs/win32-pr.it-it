---
description: MsiFiler.exe popola la tabella dei file con le versioni, le lingue e le dimensioni dei file basate su una directory di origine. Consente inoltre di aggiornare la tabella MsiFileHash con gli hash di file.
ms.assetid: cc3db60b-0b1d-4582-8b40-0b55f83e00be
title: Msifiler.exe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b2d7aeceae7abd8a9786079788e68c7d7bda35ae
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106306576"
---
# <a name="msifilerexe"></a>Msifiler.exe

MsiFiler.exe popola la [tabella dei file](file-table.md) con le versioni, le lingue e le dimensioni dei file basate su una directory di origine. Consente inoltre di aggiornare la [tabella MsiFileHash](msifilehash-table.md) con gli hash di file.

## <a name="syntax"></a>Sintassi

**msifiler.exe-d** *{database}* **\[ -v \] \[ -h \] \[ -s ALTSOURCE \]**

## <a name="command-line-options"></a>Opzioni da riga di comando

Msifiler.exe usa le seguenti opzioni della riga di comando senza distinzione tra maiuscole e minuscole. Al posto di un trattino, può essere utilizzato anche un delimitatore di barra.



| Opzione | Parametro   | Descrizione                                                                                                                                                                  |
|--------|-------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| -d     | *database*  | Il database (file con estensione msi) da aggiornare.                                                                                                                              |
| -v     |             | Usare la modalità verbose.                                                                                                                                                            |
| -H     |             | Popolare la [tabella MsiFileHash](msifilehash-table.md). Questa operazione crea la tabella se non esiste già. La tabella MsiFileHash può essere utilizzata solo con file senza versione. |
| -S     | *ALTSOURCE* | ALTSOURCE specifica una directory alternativa per trovare i file.                                                                                                              |



 

Questo strumento è disponibile solo nei [componenti Windows SDK per Windows Installer sviluppatori](platform-sdk-components-for-windows-installer-developers.md).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Strumenti di sviluppo Windows Installer](windows-installer-development-tools.md)
</dt> <dt>

[Uso della tabella di directory](using-the-directory-table.md)
</dt> <dt>

[Versioni rilasciate, strumenti e ridistribuibili](released-versions-tools-and-redistributables.md)
</dt> </dl>

 

 



