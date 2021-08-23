---
description: Windows Il programma di installazione può usare le firme digitali come mezzo per rilevare le risorse danneggiate.
ms.assetid: fc982813-583b-4fcd-88d8-9de227994e7b
title: Msicert.exe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ede88930cdb6cc616d8c39fb400f0c67c31eecd01d6d1a7d1832421cb394bcc4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119534546"
---
# <a name="msicertexe"></a>Msicert.exe

Windows Il programma di installazione può usare le firme digitali come mezzo per rilevare le risorse danneggiate. Un certificato del firmatario può essere confrontato con il certificato del firmatario di una risorsa esterna che deve essere installato dal pacchetto. Per altre informazioni, vedere [Digital Signatures and Windows Installer](digital-signatures-and-windows-installer.md).

MsiCert.exe è un'utilità della riga di comando che può essere usata per popolare la tabella [MsiDigitalSignature](msidigitalsignature-table.md) e la tabella [MsiDigitalCertificate](msidigitalcertificate-table.md) con le informazioni sulla firma digitale di un file CAB esterno. Il file CAB deve essere firmato digitalmente ed elencato nella [tabella Media](media-table.md). MsiCert.exe usa le informazioni sul certificato del firmatario dell'archivio con firma digitale e creerà e aggiungerà le tabelle MsiDigitalSignature e MsiDigitalCertificate al database, se non esistono già.

## <a name="syntax"></a>Sintassi

**msicert -d** *{database}* **-m** *{media entry}* **-c** *{cabinet}* **\[ -h \]**

## <a name="command-line-options"></a>Opzioni da riga di comando

Le opzioni della riga di comando non distinzione tra maiuscole e minuscole e i delimitatori barra possono essere usati al posto di un trattino.



| Opzione | Parametro        | Descrizione                                                                                             |
|--------|------------------|---------------------------------------------------------------------------------------------------------|
| -d     | <database> | Database (.msi file) da aggiornare.                                                         |
| -M     | <media Id> | Voce nel campo DiskId della tabella [Media nel](media-table.md) record per il file CAB. |
| -c     | <cabinet>  | Percorso del file CAB con firma digitale.                                                          |
| -H     |                  | Includere l'hash della firma digitale. Questo indirizzo è facoltativo.                                            |



 

Questo strumento è disponibile solo in componenti Windows [SDK per sviluppatori Windows Programma di installazione](platform-sdk-components-for-windows-installer-developers.md).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Windows Strumenti di sviluppo del programma di installazione](windows-installer-development-tools.md)
</dt> <dt>

[Versioni rilasciate, strumenti e ridistribuibili](released-versions-tools-and-redistributables.md)
</dt> </dl>

 

 



