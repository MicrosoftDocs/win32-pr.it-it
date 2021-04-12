---
description: Windows Installer possibile utilizzare le firme digitali come mezzo per rilevare le risorse danneggiate.
ms.assetid: fc982813-583b-4fcd-88d8-9de227994e7b
title: Msicert.exe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a0a4df800bbcfa9ed2fb0d016794b3ebcf1535be
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104234038"
---
# <a name="msicertexe"></a>Msicert.exe

Windows Installer possibile utilizzare le firme digitali come mezzo per rilevare le risorse danneggiate. Un certificato del firmatario può essere confrontato con il certificato del firmatario di una risorsa esterna da installare dal pacchetto. Per ulteriori informazioni, vedere [firme digitali e Windows Installer](digital-signatures-and-windows-installer.md).

MsiCert.exe è un'utilità della riga di comando che può essere utilizzata per popolare la tabella [MsiDigitalSignature](msidigitalsignature-table.md) e la [tabella MsiDigitalCertificate](msidigitalcertificate-table.md) con le informazioni sulla firma digitale di un file CAB esterno. Il file CAB deve essere firmato digitalmente ed elencato nella [tabella dei supporti](media-table.md). MsiCert.exe usa le informazioni sul certificato del firmatario dall'armadio con firma digitale e crea e aggiunge le tabelle MsiDigitalSignature e MsiDigitalCertificate al database, se non esistono già.

## <a name="syntax"></a>Sintassi

**msicert-d** *{database}* **-m** *{voce multimediale}* **-c** *{cabinet}* **\[ -h \]**

## <a name="command-line-options"></a>Opzioni da riga di comando

Le opzioni della riga di comando non fanno distinzione tra maiuscole e minuscole e i delimitatori di barra possono essere utilizzati al posto di un trattino.



| Opzione | Parametro        | Descrizione                                                                                             |
|--------|------------------|---------------------------------------------------------------------------------------------------------|
| -d     | <database> | Il database (file con estensione msi) in fase di aggiornamento.                                                         |
| -M     | <media Id> | Voce nel campo DiskID della [tabella dei supporti](media-table.md) nel record per il file CAB. |
| -c     | <cabinet>  | Percorso del file CAB con firma digitale.                                                          |
| -H     |                  | Includere l'hash della firma digitale. Questo indirizzo è facoltativo.                                            |



 

Questo strumento è disponibile solo nei [componenti Windows SDK per Windows Installer sviluppatori](platform-sdk-components-for-windows-installer-developers.md).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Strumenti di sviluppo Windows Installer](windows-installer-development-tools.md)
</dt> <dt>

[Versioni rilasciate, strumenti e ridistribuibili](released-versions-tools-and-redistributables.md)
</dt> </dl>

 

 



