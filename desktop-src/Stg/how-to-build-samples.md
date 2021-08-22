---
title: Come compilare esempi
description: Per compilare un esempio COM, l'ambiente del computer deve essere configurato per compilare applicazioni C++ Win32 Microsoft.
ms.assetid: c62b8b4d-a9d2-4587-8bb6-7b2c30d1c00d
keywords:
- Come compilare esempi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 782a75bb54127191757a515244d439bbff9570c96f4e0bb2ac603477bedb96a0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119663121"
---
# <a name="how-to-build-samples"></a>Come compilare esempi

Per compilare un esempio COM, l'ambiente del computer deve essere configurato per compilare applicazioni C++ Win32 Microsoft.

## <a name="preparing-a-computer-to-create-com-samples"></a>Preparazione di un computer per la creazione di esempi COM

L'ambiente del computer deve essere configurato con un compilatore C++ a 32 bit installato correttamente, un linker e un compilatore di risorse compatibili con Microsoft Visual C++ 4.x o versione successiva e un SDK Windows correttamente installato. È meglio installare la versione più Windows SDK. L Windows SDK fornisce i file di libreria con estensione h include e lib necessari per la funzionalità COM codificata negli esempi.

Per eseguire correttamente gli esempi Remclien, Freserve e Freclien, sono necessarie funzionalità di sistema disponibili nei sistemi operativi Windows: Windows Server 2003, Windows XP, Windows 2000 o Windows NT 4.0. Gli esempi Remclien, Freserve e Freclien verranno compilati ma non verranno eseguiti nei sistemi operativi Windows Me, Windows 98 o Windows 95, a meno che Distributed COM (DCOM) e FREE Threaded COM non siano parte del sistema operativo. Questo supporto è disponibile per i sistemi operativi Windows Me, Windows 98 e Windows 95 nel componente aggiuntivo DCOM95. DCOM95 può attualmente essere ottenuto [scaricando da Microsoft](https://www.microsoft.com/download/details.aspx?id=31661).

Ogni directory di esempio include i file di origine necessari per compilare ed eseguire l'esempio. La directory di esempio padre include un file Makeall.bat, che è possibile eseguire dal prompt dei comandi per creare tutti gli esempi di codice nel ramo seguente. Per altre informazioni, vedere il file Makeall.bat. Se l'ambiente è configurato per compilare applicazioni C++ Win32, è sufficiente eseguire Makeall.bat dalla directory in cui si trova per compilare tutti gli esempi di codice nel ramo seguente. Makeall garantisce l'ordine corretto per la compilazione in modo che tutte le dipendenze dell'esempio di codice siano soddisfatte.

La directory principale include anche un makefile che compila tutti gli esempi di codice dell'esercitazione usando opzioni simili a quelle supportate da Makeall.bat. Per altre informazioni, vedere questo makefile. Questo makefile presuppone che l'intero ramo di esempi di codice sia installato come parte di Windows SDK. Attualmente questo percorso ha un percorso simile a *D: \\ MSSDK \\ SAMPLES COM \\ \\ TUTSAMP*, dove D: rappresenta l'unità di installazione. Se è stato estratto il ramo di esempio di codice dell'esercitazione (ad esempio, la directory COM e le relative sottodirectory) in un'altra posizione esterna a Windows SDK (o se il set di esempi è stato ottenuto come download separato dal sito Web Microsoft), usare Makeall.bat per compilare tutti gli esempi nel ramo. In generale, è Makeall.bat consigliato. Viene Logmall.bat anche un file di configurazione. Esegue la stessa operazione del file batch Makeall, ad eccezione del fatto che registra tutto l'output di compilazione Errorlog.txt file nella directory principale dell'esercitazione.

Nella directory principale vengono inoltre forniti due file batch, Regall.bat e Unregall.bat, per registrare e annullare la registrazione di tutti i server COM nella serie di esempi di codice dell'esercitazione. Per registrare tutti i server, Regall.bat file dalla directory principale. Per annullare la registrazione di tutti i server, Unregall.bat allo stesso modo. Questi file batch richiedono una build precedente degli esempi di codice REGISTER, MARSHAL, DLLSERVE, LICSERVE, LOCSERVE, APTSERVE, FRESERVE e CONSERVE. Se si esegue una compilazione normale degli esempi di codice, i makefile del server registreranno automaticamente i server. In questo caso, non è necessario eseguire il file batch Regall.

Eseguire il Cleanall.bat batch per eseguire un cleanall completo di tutti gli esempi di esercitazioni COM.

> [!WARNING]
> Questo file batch elimina tutti i Visual Studio di progetto e altri file di lavoro temporanei creati da Visual C++ negli esempi. Tutti i server COM compilati negli esempi di codice dell'esercitazione vengono annullati dal Registro di sistema. Tutti i file exe e .dll eseguibili vengono eliminati. Tutti i file di simboli di debug vengono eliminati. Vengono eliminati anche i file generati in un'ampia gamma di ambienti di compilazione.

 

Eseguire "Makeall Clean" per eseguire una pulizia più veloce, ma più semplice, di tutti gli esempi di codice. Questa operazione di pulizia non tenta di essere completa come quella eseguita da Cleanall.bat. I file obj vengono eliminati, ma i file binari di output vengono mantenuti. La registrazione dei server COM non viene annullata dal Registro di sistema.

Questa serie di esempio è stata originata come parte integrante di Windows SDK, pertanto la narrazione dell'esercitazione presuppone un ambiente con Windows SDK installato correttamente.

Tuttavia, le versioni Microsoft Visual C++ versione 4.0 e successive possono fornire anche i file di libreria con estensione h include e lib necessari per la compilazione. In questi casi, l'installazione dell Windows SDK potrebbe non essere necessaria per compilare gli esempi.

Per altre informazioni e per informazioni complete sulla compilazione di esempio, vedere:

[Configurazione dell'ambiente](environment-setup.md)

[Makefile](makefiles.md)

[Con Visual Studio](using-visual-studio.md)

[Estrazione degli esempi di codice](extracting-the-code-samples.md)

[Convenzioni di stile di codifica](coding-style-conventions.md)

 

 




