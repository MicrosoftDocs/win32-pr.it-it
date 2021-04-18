---
title: Come compilare esempi
description: Per compilare un esempio COM, è necessario configurare l'ambiente del computer per la compilazione di applicazioni Microsoft Win32 C++.
ms.assetid: c62b8b4d-a9d2-4587-8bb6-7b2c30d1c00d
keywords:
- Come compilare esempi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 593d3465d3ebcc32a6768dd8b2dffe1f0a653d07
ms.sourcegitcommit: c2a1c4314550ea9bd202d28adfcc7bfe6180932f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/11/2020
ms.locfileid: "106299535"
---
# <a name="how-to-build-samples"></a>Come compilare esempi

Per compilare un esempio COM, è necessario configurare l'ambiente del computer per la compilazione di applicazioni Microsoft Win32 C++.

## <a name="preparing-a-computer-to-create-com-samples"></a>Preparazione di un computer per la creazione di esempi COM

L'ambiente del computer deve essere configurato con un compilatore C++ a 32 bit installato correttamente, un linker e un compilatore di risorse compatibili con Microsoft Visual C++ 4. x o versione successiva e una Windows SDK installata correttamente. È preferibile installare il Windows SDK ultimo. Il Windows SDK include i file di libreria con estensione h e lib necessari per la funzionalità COM codificata negli esempi.

Per eseguire correttamente gli esempi Remclien, Freserve e Freclien, sono necessarie funzionalità di sistema disponibili nei sistemi operativi Windows: Windows Server 2003, Windows XP, Windows 2000 o Windows NT 4,0. Gli esempi Remclien, Freserve e Freclien verranno compilati, ma non verranno eseguiti nei sistemi operativi Windows me, Windows 98 o Windows 95, a meno che il sistema operativo non distribuisca com (DCOM) e COM a thread libero. Questo supporto è disponibile per i sistemi operativi Windows me, Windows 98 e Windows 95 nel componente aggiuntivo DCOM95. Attualmente è possibile ottenere DCOM95 tramite [download da Microsoft](https://www.microsoft.com/download/details.aspx?id=31661).

Ogni directory di esempio include i file di origine necessari per compilare ed eseguire l'esempio. La directory di esempio padre dispone di un file di Makeall.bat, che è possibile eseguire dal prompt dei comandi per eseguire tutti gli esempi di codice nel ramo riportato di seguito. Per ulteriori informazioni, vedere il file di Makeall.bat. Se l'ambiente è configurato per la compilazione di applicazioni C++ Win32, è possibile eseguire semplicemente Makeall.bat dalla directory in cui risiede per compilare tutti gli esempi di codice nel branch seguente. Makeall garantisce l'ordine corretto per la compilazione in modo che tutte le dipendenze di esempio di codice siano soddisfatte.

La directory principale dispone anche di un makefile che compila tutti gli esempi di codice dell'esercitazione usando opzioni simili a quelle supportate da Makeall.bat. Per ulteriori informazioni, vedere questo makefile. Questo Makefile presuppone che l'intero ramo esempi di codice sia installato come parte del Windows SDK. Attualmente questo percorso ha un percorso simile a *d: \\ MSSDK \\ Samples \\ com \\ TUTSAMP*, dove d: rappresenta l'unità di installazione. Se è stato estratto il ramo di esempio di codice dell'esercitazione (ad esempio, la directory com e le relative sottodirectory) in un'altra posizione all'esterno del Windows SDK (o se è stato ottenuto il set di esempio come download separato dal sito Web Microsoft), usare Makeall.bat per compilare tutti gli esempi nel ramo. In generale, è consigliabile Makeall.bat. Viene inoltre fornito un file di Logmall.bat. Esegue la stessa operazione del file batch makeall, ad eccezione del fatto che registra tutti gli output di compilazione in file Errorlog.txt nella directory principale dell'esercitazione.

Due file batch, Regall.bat e Unregall.bat, vengono forniti nella directory principale per registrare e annullare la registrazione di tutti i server COM nella serie di esempi di codice dell'esercitazione. Per registrare tutti i server, eseguire Regall.bat file dalla directory principale. Per annullare la registrazione di tutti i server, eseguire Unregall.bat nello stesso modo. Questi file batch richiedono una compilazione precedente degli esempi di codice REGISTER, MARSHAL, DLLSERVE, LICSERVE, LOCSERVE, APTSERVE, FRESERVE e conserve. Se si esegue una build normale degli esempi di codice, i makefile del server registreranno automaticamente i server. In questo caso, non è necessario eseguire il file batch Regal.

Eseguire il file batch Cleanall.bat per eseguire un cleanall completo di tutti gli esempi di esercitazione COM.

> [!WARNING]
> Questo file batch Elimina tutti i file di progetto di Visual Studio e altri file di lavoro temporanei creati da Visual C++ negli esempi. A tutti i server COM incorporati negli esempi di codice dell'esercitazione viene annullata la registrazione dal registro di sistema. Tutti i file exe e dll eseguibili vengono eliminati. Tutti i file di simboli di debug vengono eliminati. Vengono eliminati anche i file generati in un'ampia gamma di ambienti di compilazione.

 

Eseguire ' makeall clean ' per eseguire una pulizia più veloce, ma più modesta, di tutti gli esempi di codice. Questa operazione di pulizia non tenta di essere completa come quella eseguita da Cleanall.bat. I file con estensione obj vengono eliminati, ma i file binari di output vengono conservati. Non è stata annullata la registrazione dei server COM dal registro di sistema.

Questa serie di esempi è stata originata come parte integrante del Windows SDK, pertanto nella descrizione dell'esercitazione si presuppone che un ambiente con la Windows SDK installata correttamente.

Tuttavia, le versioni di Microsoft Visual C++ versione 4,0 e successive possono fornire anche i file di libreria con estensione h e lib necessari per la compilazione. In questi casi, l'installazione del Windows SDK potrebbe non essere necessaria per compilare gli esempi.

Per ulteriori informazioni e dettagli completi sulla compilazione di esempio, vedere:

[Configurazione dell'ambiente](environment-setup.md)

[Makefile](makefiles.md)

[Con Visual Studio](using-visual-studio.md)

[Estrazione degli esempi di codice](extracting-the-code-samples.md)

[Convenzioni di stile di codifica](coding-style-conventions.md)

 

 




