---
description: Il file VBScript Manifestchk.vbs è uno strumento di convalida disponibile in Microsoft Windows Software Development Kit (SDK) che convalida i file manifesto dell'applicazione e dell'assembly.
ms.assetid: 8269cb92-bd3f-411f-8395-fe06ed550cc5
title: Manifestchk.vbs
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 09aff347fbd8b6f44c4e38f123870fa5ee8df572
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104401696"
---
# <a name="manifestchkvbs"></a>Manifestchk.vbs

Il file VBScript Manifestchk.vbs è uno strumento di convalida disponibile in Microsoft Windows Software Development Kit (SDK) che convalida i file manifesto dell'applicazione e dell'assembly.

Per eseguire questo esempio è necessario Windows script host. Per ulteriori informazioni su Windows script host, vedere la sezione Windows script host del Windows SDK. Windows script host è in realtà costituito da due host. CScript.exe è la versione che consente di eseguire gli script dal prompt dei comandi. CScript.exe fornisce opzioni della riga di comando per l'impostazione delle proprietà dello script.

Il formato della riga di comando è il seguente:

**Cscript//NoLogo manifestchk.vbs/s:** *\[ unità: \] \[ percorso \] schemafilename* **/m:** *\[ unità: \] \[ percorso \] ManifestFileName* **\[ /q \] /t:** *opzione*

I flag definiti per Manifestchk.vbs sono descritti nella tabella seguente.



| Flag | Descrizione                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
|------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| /s   | Specifica il nome del file di schema del manifesto rispetto al quale convalidare i manifesti. Vedere lo schema nello [schema del file manifesto](manifest-file-schema.md).                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| /m   | Specifica il nome del file manifesto da convalidare.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| /q   | Disattiva tutto l'output nella console.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| /t   | Specifica il tipo di file manifesto. I valori validi sono: AM Validate the [manifest file schema](manifest-file-schema.md) of a [assembly manifest](assembly-manifests.md) o [Application Manifest](application-manifests.md)<br/> PC convalida lo [schema del file di configurazione](publisher-configuration-file-schema.md) dell'editore di un [file di configurazione del server di pubblicazione](publisher-configuration-files.md)<br/> AC convalida lo schema del file di configurazione dell'applicazione di un [file di configurazione dell'applicazione](application-configuration-files.md).<br/> |



 

Se il flag/q non è specificato, Manifestchk.vbs Visualizza informazioni dettagliate sul primo errore rilevato nel file e visualizza un messaggio che indica se il processo di convalida ha avuto esito positivo o negativo.

Questa utilità verifica quanto segue:

-   Riga di comando valida.
-   È installato MSXML versione 3.
-   Il manifesto utilizza codice XML ben formato.
-   Che il manifesto acconsente allo schema fornito. Si noti che Manifestchk.vbs verifica il file manifesto solo in base a quanto specificato nello schema fornito. Per un esempio di schema del manifesto, vedere [schema del file manifesto](manifest-file-schema.md).

Cscript.exe restituisce il valore 0 se il processo di convalida ha avuto esito positivo e 1 in caso di esito negativo. Restituisce 2 Se si verifica un errore in un argomento della riga di comando.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Strumenti di sviluppo di assembly affiancati](side-by-side-assembly-development-tools.md)
</dt> </dl>

 

 




