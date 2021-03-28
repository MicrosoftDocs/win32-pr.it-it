---
description: Nell'esempio seguente, una società di sviluppo software ipotetica denominata Litware, Inc.
ms.assetid: e4392907-a84f-40ea-aa88-2ad0510bca3c
title: Esempio di associazione di file
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7f4104c9bc241fed4bc698bd150b03d32a70e054
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104127867"
---
# <a name="file-association-example"></a>Esempio di associazione di file

Nell'esempio seguente, una società di sviluppo software ipotetica denominata Litware, Inc. crea un nuovo lettore audio denominato LitwarePlayer. Litware vuole progettare un'associazione di file tra LitwarePlayer e il tipo di file primario, che usa un formato audio appena sviluppato che consente l'archiviazione di un intero CD audio in meno di 10 kilobyte di memoria senza perdita di qualità.

> [!IMPORTANT]
> Questo argomento non è applicabile a Windows 10. Il modo in cui le associazioni di file predefinite cambiano in Windows 10. Per ulteriori informazioni, vedere la sezione relativa alle **modifiche apportate al modo in cui Windows 10 gestisce le app predefinite** in [questo post](https://blogs.windows.com/bloggingwindows/2015/05/20/announcing-windows-10-insider-preview-build-10122-for-pcs/).

 

## <a name="designing-a-new-file-association"></a>Progettazione di una nuova associazione di file

La società deve eseguire i passaggi seguenti.

1.  **Decidere se il nuovo tipo di file deve essere considerato pubblico o privato.** Questo nuovo tipo di file è un tipo di supporto. Poiché gli utenti scambiano file multimediali su diverse piattaforme e potrebbero essere presenti altre applicazioni che devono leggere il formato LitwarePlayer, un tipo di file [pubblico](fa-file-types.md) è il più appropriato.
2.  **Determinare se il tipo di file è già definito.** Controllare il database MIME IANA (Internet Assigned Numbers Authority) e altri database dei tipi di file pubblici su Internet per determinare che non è stato definito alcun tipo di file analogo. Poiché si tratta di un nuovo formato di file, è necessario definire un nuovo tipo di file.
3.  **Definire un'estensione del nome file per il nuovo tipo di file.** Gli sviluppatori scelgono `.opa-ltw-audio` , che incorpora l'abbreviazione del fornitore e un suggerimento sul contenuto del file. La ricerca determina che l'estensione non è usata da altri utenti. Seguendo le raccomandazioni correnti, non viene definita alcuna estensione breve.
4.  **Definire un tipo MIME per il tipo di file e registrarlo con IANA.** Litware definisce il nuovo tipo MIME come *audio/LitwarePlayer. 1* e prepara un'applicazione di tipo MIME, seguendo le linee guida previste nei numeri RFC (Request for Comments) 2045, 2046, 2047 e 2048. Quindi inviano l'applicazione a IANA, che aggiunge il nuovo tipo di file al database dei tipi MIME registrati.
5.  **Determinare se esiste un ProgID per il tipo di file.** Poiché si tratta di un nuovo tipo di file, non esiste alcun [ProgID](fa-progids.md) . Litware imposta sulla progettazione di un nuovo ProgID per LitwarePlayer. Decidono il nome descrittivo "LitwarePlayer Audio Player" (archiviato come risorsa nel file LitwarePlayer.exe) e progettano un'icona predefinita da usare per i file associati a LitwarePlayer (archiviati anche in LitwarePlayer.exe). Poiché LitwarePlayer è una nuova applicazione, si tratta di un ProgID della versione 1.
6.  **Registrare il ProgID.** Quando LitwarePlayer è installato, il programma di installazione crea la voce [ProgID](fa-progids.md) seguente nel registro di sistema.

    ```
    HKEY_CLASSES_ROOT
       Litware.LitwarePlayer.1
          (Default) = LitwarePlayer Audio Player
          FriendlyTypeName = @LitwarePlayer, -120
          CurVer
             (Default) = Litware.LitwarePlayer.1
          DefaultIcon
             (Default) = LitwarePlayer, -142
          shell
             play
                command
                   (Default) = "%ProgramFiles%\LitwarePlayer\LitwarePlayer.exe" "%1"
    ```

    Nella chiave del comando %1 viene passato come percorso del file da riprodurre.

7.  **Registrare l'estensione del nome file per il tipo di file.** Quando LitwarePlayer è installato, il programma di installazione crea le seguenti voci nel registro di sistema per l'estensione del tipo di file personalizzato.

    ```
    HKEY_CLASSES_ROOT
       .opa-vwi-audio
          (Default) = Litware.LitwarePlayer.1
          PerceivedType = Audio
          Content Type = audio/LitwarePlayer
    ```

> [!Note]  
> Ogni volta che viene creata o modificata un'associazione di file, notificare al sistema che è stata apportata una modifica chiamando [**SHChangeNotify**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shchangenotify), specificando l' \_ evento SHCNE ASSOCCHANGED. Se questa operazione non viene eseguita, è possibile che la shell non riconosca le modifiche apportate fino al riavvio del sistema.

 

## <a name="additional-resources"></a>Risorse aggiuntive

-   [Introduzione alle associazioni di file](fa-intro.md)
-   [Come registrare un browser Internet o un client di posta elettronica con il menu Start di Windows](start-menu-reg.md)
-   [Registrazione di un'applicazione in uno schema URI](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa767914(v=vs.85))

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Procedure consigliate per le associazioni di file](fa-best-practices.md)
</dt> <dt>

[Linee guida per la gestione di applicazioni predefinite in Windows Vista e versioni successive](vista-managing-defaults.md)
</dt> <dt>

[Programmi predefiniti](default-programs.md)
</dt> <dt>

[Impostazione dell'accesso al programma e delle impostazioni predefinite del computer (SPAD)](cpl-setprogramaccess.md)
</dt> </dl>

 

 
