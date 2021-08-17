---
description: Il file VBScript Manifestchk.vbs è uno strumento di convalida disponibile in Microsoft Windows Software Development Kit (SDK) che convalida i file manifesto dell'applicazione e dell'assembly.
ms.assetid: 8269cb92-bd3f-411f-8395-fe06ed550cc5
title: Manifestchk.vbs
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 686843d1b4ab099d44a33b715f65564a12834f54ed6e8f62310df0aedbe53de1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119142054"
---
# <a name="manifestchkvbs"></a>Manifestchk.vbs

Il file VBScript Manifestchk.vbs è uno strumento di convalida disponibile in Microsoft Windows Software Development Kit (SDK) che convalida i file manifesto dell'applicazione e dell'assembly.

L'esecuzione di questo esempio Windows Host script. Per altre informazioni su Windows Host script, vedere la sezione Windows Script Host (Host script di Windows) di Windows SDK. Windows L'host di script è in realtà due host. CScript.exe è la versione che consente di eseguire script dal prompt dei comandi. CScript.exe opzioni della riga di comando per l'impostazione delle proprietà dello script.

Il formato della riga di comando è il seguente:

**Cscript //nologo manifestchk.vbs /s: unità:** percorso *\[ \] \[ \] nomefile* schema **/m:** *\[ unità: \] \[ percorso \] manifestfilename* **\[ /q \] /t:** *opzione*

I flag definiti per Manifestchk.vbs sono descritti nella tabella seguente.



| Flag | Descrizione                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
|------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| /s   | Specifica il nome del file di schema del manifesto rispetto al quale convalidare i manifesti. Vedere lo schema in [Schema del file manifesto.](manifest-file-schema.md)                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| /m   | Specifica il nome del file manifesto da convalidare.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| /q   | Elimina tutto l'output nella console.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| /t   | Specifica il tipo di file manifesto. I valori validi sono: AM Validate the [manifest file schema](manifest-file-schema.md) of an assembly [manifest](assembly-manifests.md) or [application manifest](application-manifests.md)<br/> PC Convalidare lo [schema del file di configurazione dell'editore](publisher-configuration-file-schema.md) di un file di configurazione [dell'editore](publisher-configuration-files.md)<br/> AC Convalidare lo schema del file di configurazione dell'applicazione di un [file di configurazione dell'applicazione](application-configuration-files.md).<br/> |



 

Se il flag /q non è specificato, Manifestchk.vbs visualizza informazioni dettagliate sul primo errore rilevato nel file e visualizza un messaggio che indica se il processo di convalida è stato completato o meno.

Questa utilità verifica quanto segue:

-   Riga di comando valida.
-   Questa MSXML versione 3 è installata.
-   Che il manifesto usi xml ben formato.
-   Che il manifesto sia d'accordo con lo schema fornito. Si noti Manifestchk.vbs verifica il file manifesto solo in base a quanto specificato nello schema fornito. Per un esempio di schema del manifesto, vedere [Schema del file manifesto.](manifest-file-schema.md)

Cscript.exe restituisce il valore 0 se il processo di convalida ha avuto esito positivo e 1 in caso di esito negativo. Restituisce 2 se si verifica un errore in un argomento della riga di comando.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Strumenti di sviluppo di assembly side-by-side](side-by-side-assembly-development-tools.md)
</dt> </dl>

 

 




