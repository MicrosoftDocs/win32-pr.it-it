---
description: Windows Il programma di installazione può usare le firme digitali come mezzo per rilevare le risorse danneggiate.
ms.assetid: fc982813-583b-4fcd-88d8-9de227994e7b
title: Msicert.exe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c1dbe8366093418e74ed4ab1cb8e8c23fb8036eb
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/26/2021
ms.locfileid: "122879741"
---
# <a name="msicertexe"></a>Msicert.exe

Windows Il programma di installazione può usare le firme digitali come mezzo per rilevare le risorse danneggiate. Un certificato del firmatario può essere confrontato con il certificato del firmatario di una risorsa esterna che deve essere installato dal pacchetto. Per altre informazioni, vedere [Firme digitali e Windows installer](digital-signatures-and-windows-installer.md).

MsiCert.exe è un'utilità della riga di comando che può essere usata per popolare la tabella [MsiDigitalSignature](msidigitalsignature-table.md) e la tabella [MsiDigitalCertificate](msidigitalcertificate-table.md) con le informazioni di firma digitale di un file CAB esterno. Il file cab deve essere firmato digitalmente ed elencato nella [tabella Media](media-table.md). MsiCert.exe usa le informazioni sul certificato del firmatario dall'archivio con firma digitale e creerà e aggiungerà le tabelle MsiDigitalSignature e MsiDigitalCertificate al database, se non esistono già.

## <a name="syntax"></a>Sintassi

**msicert -d** *{database}* **-m** *{media entry}* **-c** *{cabinet}* **\[ -h \]**

## <a name="command-line-options"></a>Opzioni da riga di comando

Le opzioni della riga di comando non fa distinzione tra maiuscole e minuscole e possono essere usati delimitatori di barra anziché un trattino.



| Opzione | Parametro        | Descrizione                                                                                             |
|--------|------------------|---------------------------------------------------------------------------------------------------------|
| -d     | &lt;database&gt; | Database (.msi file) da aggiornare.                                                         |
| -M     | <media Id> | Voce nel campo DiskId della tabella [Media](media-table.md) nel record per il file cab. |
| -c     | &lt;archivio&gt;  | Percorso del file CAB con firma digitale.                                                          |
| -H     |                  | Includere l'hash della firma digitale. Questo indirizzo è facoltativo.                                            |



 

Questo strumento è disponibile solo nei componenti di [Windows SDK per Windows programma di installazione](platform-sdk-components-for-windows-installer-developers.md).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Windows Strumenti di sviluppo del programma di installazione](windows-installer-development-tools.md)
</dt> <dt>

[Versioni rilasciate, strumenti e ridistribuibili](released-versions-tools-and-redistributables.md)
</dt> </dl>

 

 



