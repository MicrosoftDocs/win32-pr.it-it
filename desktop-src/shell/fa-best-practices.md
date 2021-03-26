---
description: Di seguito sono elencate le procedure consigliate da utilizzare quando si utilizzano le associazioni di file.
title: Procedure consigliate per le associazioni di file
ms.topic: article
ms.date: 05/31/2018
ms.assetid: d4d0edf9-3475-4164-b0fa-15006e05e242
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: f49c1df6d145c32b8fcbdf70462b30f14f51b3d3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104525795"
---
# <a name="best-practices-for-file-associations"></a>Procedure consigliate per le associazioni di file

Di seguito sono elencate le procedure consigliate da utilizzare quando si utilizzano le associazioni di file.

-   [Non copiare le associazioni di file dal registro di sistema](#do-not-copy-file-associations-from-the-registry)
-   [Evitare Hard-Coding percorsi nel registro di sistema laddove possibile](#avoid-hard-coding-paths-into-the-registry-where-possible)
-   [Racchiudere sempre le stringhe in espansione tra virgolette](#always-wrap-expanding-strings-in-quotation-marks)
-   [Non confondere AutoPlay/autorun con le associazioni di file](#do-not-confuse-autoplayautorun-with-file-associations)
-   [Non confondere il database MIME di Internet Explorer con le associazioni di file](#do-not-confuse-the-internet-explorer-mime-database-with-file-associations)
-   [Usare ProgID correttamente formattati e con versione](#use-properly-formed-and-versioned-progids)
-   [Non usare estensioni di file brevi](#do-not-use-short-file-name-extensions)
-   [Registrare nuovi tipi di file nel database MIME IANA](#register-new-file-types-in-the-iana-mime-database)
-   [Iscriversi con il servizio Web Windows per le associazioni di file](#sign-up-with-the-windows-web-service-for-file-associations)
-   [Argomenti correlati](#related-topics)

## <a name="do-not-copy-file-associations-from-the-registry"></a>Non copiare le associazioni di file dal registro di sistema

Si consiglia di non copiare le associazioni di file esistenti dal registro di sistema. Questo comporta spesso la propagazione di associazioni di file in formato non corretto. Al contrario, è necessario seguire i passaggi descritti in [scenario di esempio di associazione di file](fa-sample-scenarios.md).

## <a name="avoid-hard-coding-paths-into-the-registry-where-possible"></a>Evitare Hard-Coding percorsi nel registro di sistema laddove possibile

Analogamente a quanto i percorsi di programmazione dei programmi possono causare problemi, i percorsi hardcoded nel registro di sistema possono causare anche problemi. È invece consigliabile utilizzare le stringhe di espansione del registro di sistema (REG \_ expand \_ SZ) per fornire l'indipendenza del percorso ove applicabile. Ad esempio, invece di usare questo metodo:

```
HKEY_CLASSES_ROOT
   MyVendor.MyProgram.1
      DefaultIcon
         (Default) = C:\WINNT\hta.exe,1
```

Usare questo metodo:

```
HKEY_CLASSES_ROOT
   MyVendor.MyProgram.1
      DefaultIcon
         (Default) = "%SYSTEMROOT%\hta.exe,1"
```

## <a name="always-wrap-expanding-strings-in-quotation-marks"></a>Racchiudere sempre le stringhe in espansione tra virgolette

Le stringhe di espansione possono contenere spazi quando si espandono. Poiché gli spazi vengono spesso interpretati come delimitatori di argomento, causano problemi in determinate circostanze. Ad esempio, un comando per richiamare il programma può essere archiviato nel registro di sistema come segue:

`%SYSTEMROOT%\MyProgram %1 %2`

In programma si prevede che %1 sia il percorso completo di un nome file e %2 è un'opzione per indicare un'azione. Se questo comando viene eseguito con gli argomenti **c: \\ Program Files \\ \\document.txt** e **/Print** e supponendo una SystemRoot di c: \\ WinNT, si espande a:

`C:\WINNT\MyProgram C:\Program Files\My Documents\document.txt /print`

In questo caso, il programma indica che il primo argomento è C: \\ Program e il secondo argomento è file \\ My, che non è il comportamento previsto. Gli argomenti vengono interpretati correttamente, tuttavia, indipendentemente dal fatto che contengano spazi, se le stringhe in espansione sono racchiuse tra virgolette come indicato di seguito:

`"%SYSTEMROOT%\MyProgram" "%1" "%2"`

## <a name="do-not-confuse-autoplayautorun-with-file-associations"></a>Non confondere AutoPlay/autorun con le associazioni di file

Le associazioni di file sono simili a AutoPlay/autorun in alcuni modi. Tuttavia, AutoPlay/autorun offre funzionalità separate e distinte da quelle fornite dalle associazioni di file. Per altre informazioni, vedere [creazione di un'applicazione CD-ROM abilitata per l'esecuzione automatica](autoplay.md).

## <a name="do-not-confuse-the-internet-explorer-mime-database-with-file-associations"></a>Non confondere il database MIME di Internet Explorer con le associazioni di file

Le associazioni di file sono simili al database MIME di Windows Internet Explorer, in quanto i tipi di file possono (e dovrebbero) includere una definizione di tipo MIME. Tuttavia, il database MIME di Internet Explorer è separato e distinto dalle associazioni di file.

## <a name="use-properly-formed-and-versioned-progids"></a>Usare ProgID correttamente formattati e con versione

Usare sempre [ProgID con versione](fa-progids.md), anche se è presente una sola versione del ProgID. I ProgID con versione consentono di evitare conflitti e sovrascritture ProgID. Consentono inoltre di coesistere versioni diverse di un'applicazione.

## <a name="do-not-use-short-file-name-extensions"></a>Non usare estensioni di file brevi

Le estensioni dei nomi di file lunghi offrono i vantaggi seguenti:

-   La lunghezza limitata delle estensioni brevi le rende soggette a *collisioni di estensione.* Una collisione di estensione si verifica quando viene usata la stessa estensione per classificare più tipi di file. L'utilizzo di estensioni lunghe comporta una riduzione significativa delle probabilità che si verifichi un conflitto.
-   I nomi di file brevi tendono a essere piuttosto criptici. Le estensioni lunghe tendono a essere più significative perché è possibile incorporare informazioni aggiuntive nell'estensione.

Per ulteriori informazioni, vedere [estensioni di file](fa-file-extensions.md).

## <a name="register-new-file-types-in-the-iana-mime-database"></a>Registrare nuovi tipi di file nel database MIME IANA

IANA (Internet Assigned Numbers Authority) mantiene un database pubblico di tipi MIME registrati. Quando si definisce un nuovo tipo di file pubblico, è consigliabile definire anche un tipo MIME per il tipo di file e registrare questo tipo con IANA. Non è previsto alcun costo per la registrazione.

## <a name="sign-up-with-the-windows-web-service-for-file-associations"></a>Iscriversi con il servizio Web Windows per le associazioni di file

Gli sviluppatori di applicazioni possono iscriversi al servizio Web Windows usato dagli utenti per trovare applicazioni che possono operare su tipi di file specifici. Il processo per l'iscrizione al servizio Web è descritto in dettaglio nel [processo di onboarding del sistema di associazione file di Windows](https://support.microsoft.com/kb/929149).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Scenario di esempio di associazione di file](fa-sample-scenarios.md)
</dt> <dt>

[Linee guida per la gestione di applicazioni predefinite in Windows Vista e versioni successive](vista-managing-defaults.md)
</dt> <dt>

[Programmi predefiniti](default-programs.md)
</dt> <dt>

[Impostazione dell'accesso al programma e delle impostazioni predefinite del computer (SPAD)](cpl-setprogramaccess.md)
</dt> </dl>

 

 



