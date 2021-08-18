---
description: Di seguito sono elencate le procedure consigliate da usare quando si usano le associazioni di file.
title: Procedure consigliate per le associazioni di file
ms.topic: article
ms.date: 05/31/2018
ms.assetid: d4d0edf9-3475-4164-b0fa-15006e05e242
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 8cfa57faea9423af31e494c37d97af2b61d690095fb669a6a9b47109f6e97e70
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119094216"
---
# <a name="best-practices-for-file-associations"></a>Procedure consigliate per le associazioni di file

Di seguito sono elencate le procedure consigliate da usare quando si usano le associazioni di file.

-   [Non copiare associazioni di file dal Registro di sistema](#do-not-copy-file-associations-from-the-registry)
-   [Evitare Hard-Coding percorsi nel Registro di sistema laddove possibile](#avoid-hard-coding-paths-into-the-registry-where-possible)
-   [Racchiudere sempre le stringhe di espansione tra virgolette](#always-wrap-expanding-strings-in-quotation-marks)
-   [Non confondere riproduzione automatica/esecuzione automatica con associazioni di file](#do-not-confuse-autoplayautorun-with-file-associations)
-   [Non confondere il Internet Explorer MIME con le associazioni di file](#do-not-confuse-the-internet-explorer-mime-database-with-file-associations)
-   [Usare progID con formato corretto e con controllo delle versioni](#use-properly-formed-and-versioned-progids)
-   [Non usare estensioni di file brevi](#do-not-use-short-file-name-extensions)
-   [Registrare nuovi tipi di file nel database MIME IANA](#register-new-file-types-in-the-iana-mime-database)
-   [Iscriversi al servizio Web Windows per le associazioni di file](#sign-up-with-the-windows-web-service-for-file-associations)
-   [Argomenti correlati](#related-topics)

## <a name="do-not-copy-file-associations-from-the-registry"></a>Non copiare associazioni di file dal Registro di sistema

È consigliabile non copiare le associazioni di file esistenti dal Registro di sistema. Ciò comporta spesso la propagazione di associazioni di file in formato non corretto. È invece necessario seguire i passaggi descritti in [Scenario di esempio di associazione file](fa-sample-scenarios.md).

## <a name="avoid-hard-coding-paths-into-the-registry-where-possible"></a>Evitare Hard-Coding percorsi nel Registro di sistema laddove possibile

Così come i percorsi hard-cod nei programmi possono causare problemi, anche i percorsi hard-cod nel Registro di sistema possono causare problemi. È invece consigliabile usare le stringhe di espansione del Registro di sistema (REG \_ EXPAND \_ SZ) per garantire l'indipendenza del percorso, se applicabile. Ad esempio, anziché usare questo metodo:

```
HKEY_CLASSES_ROOT
   MyVendor.MyProgram.1
      DefaultIcon
         (Default) = C:\WINNT\hta.exe,1
```

È consigliabile usare questo metodo:

```
HKEY_CLASSES_ROOT
   MyVendor.MyProgram.1
      DefaultIcon
         (Default) = "%SYSTEMROOT%\hta.exe,1"
```

## <a name="always-wrap-expanding-strings-in-quotation-marks"></a>Racchiudere sempre le stringhe di espansione tra virgolette

Le stringhe di espansione possono contenere spazi quando si espandono. Poiché gli spazi vengono spesso interpretati come delimitatori di argomento, causano problemi in determinate circostanze. Ad esempio, un comando per richiamare MyProgram può essere archiviato nel Registro di sistema come:

`%SYSTEMROOT%\MyProgram %1 %2`

MyProgram prevede che %1 sia il percorso completo di un nome di file e %2 è un'opzione per indicare un'azione. Se questo comando viene eseguito con gli argomenti C: Programmi **\\ Documenti \\ \\document.txt** e **/print** e presupponendo che systemROOT sia C: WINNT, si espande \\ in:

`C:\WINNT\MyProgram C:\Program Files\My Documents\document.txt /print`

In questo caso, MyProgram interpreta che il primo argomento è C: Program e il secondo argomento è Files My, che \\ non è il comportamento \\ previsto. Gli argomenti vengono interpretati correttamente, tuttavia, indipendentemente dal fatto che contengano spazi, se le stringhe di espansione vengono racchiuse tra virgolette come indicato di seguito:

`"%SYSTEMROOT%\MyProgram" "%1" "%2"`

## <a name="do-not-confuse-autoplayautorun-with-file-associations"></a>Non confondere riproduzione automatica/esecuzione automatica con associazioni di file

Le associazioni di file sono simili per alcuni aspetti alla riproduzione automatica o all'esecuzione automatica. Tuttavia, Autoplay/Autorun offre funzionalità separate e distinte da quelle fornite dalle associazioni di file. Per altre informazioni, vedere [Creazione di un'applicazione CD-ROM abilitata per l'esecuzione automatica.](autoplay.md)

## <a name="do-not-confuse-the-internet-explorer-mime-database-with-file-associations"></a>Non confondere il Internet Explorer MIME con le associazioni di file

Le associazioni di file sono simili Windows Internet Explorer database MIME, in cui i tipi di file possono (e devono) includere una definizione di tipo MIME. Tuttavia, il Internet Explorer MIME è separato e distinto dalle associazioni di file.

## <a name="use-properly-formed-and-versioned-progids"></a>Usare progID con formato corretto e con controllo delle versioni

Usare sempre [i ProgID con controllo delle](fa-progids.md)versioni, anche se è presente una sola versione di ProgID. I ProgID con controllo delle versioni consentono di evitare conflitti e sovrascrittura di ProgID. Consentono anche la coesistenza di versioni diverse di un'applicazione.

## <a name="do-not-use-short-file-name-extensions"></a>Non usare estensioni di file brevi

Le estensioni di file lunghe offrono i vantaggi seguenti:

-   La lunghezza limitata delle estensioni brevi le rende rischiose da *conflitti di estensione.* Si verifica un conflitto di estensione quando la stessa estensione viene usata per classificare più tipi di file. L'uso di estensioni lunghe riduce significativamente le probabilità di collisione.
-   I nomi di file brevi tendono a essere piuttosto criptici. Le estensioni lunghe tendono a essere più significative perché è possibile incorporare informazioni aggiuntive nell'estensione.

Per altre informazioni, vedere [Estensioni di file.](fa-file-extensions.md)

## <a name="register-new-file-types-in-the-iana-mime-database"></a>Registrare nuovi tipi di file nel database MIME IANA

Internet Assigned Numbers Authority (IANA) mantiene un database pubblico di tipi MIME registrati. Quando si definisce un nuovo tipo di file pubblico, è consigliabile definire anche un tipo MIME per il tipo di file e registrarlo con IANA. Non è previsto alcun costo per la registrazione.

## <a name="sign-up-with-the-windows-web-service-for-file-associations"></a>Iscriversi al servizio Web Windows per le associazioni di file

Gli sviluppatori di applicazioni possono iscriversi al servizio Web Windows che gli utenti usano per trovare le applicazioni che possono operare su tipi di file specifici. Il processo di registrazione al servizio Web è descritto in dettaglio Windows [on-boarding](https://support.microsoft.com/kb/929149)di File Association System.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Scenario di esempio di associazione file](fa-sample-scenarios.md)
</dt> <dt>

[Linee guida per la gestione delle applicazioni predefinite in Windows Vista e versioni successive](vista-managing-defaults.md)
</dt> <dt>

[Programmi predefiniti](default-programs.md)
</dt> <dt>

[Impostare l'accesso ai programmi e le impostazioni predefinite del computer (SPAD)](cpl-setprogramaccess.md)
</dt> </dl>

 

 



