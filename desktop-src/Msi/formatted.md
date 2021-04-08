---
description: Il tipo di dati formattato è una stringa di testo che viene elaborata per risolvere i nomi di proprietà incorporati, le chiavi della tabella, i riferimenti alle variabili di ambiente e altre sottostringhe speciali.
ms.assetid: 7a1bc160-a06c-4d57-b429-e39167893a45
title: Formattazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cdd15dca46839b25dbf186d8a741b7a5c37c05f3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103967805"
---
# <a name="formatted"></a>Formattazione

Il tipo di dati formattato è una stringa di testo che viene elaborata per risolvere i nomi di proprietà incorporati, le chiavi della tabella, i riferimenti alle variabili di ambiente e altre sottostringhe speciali. Per risolvere la stringa sono state riconosciute le convenzioni seguenti:

-   \[ \] Nel testo rimangono le parentesi quadre () o le parentesi graffe ({}) senza coppia corrispondente.
-   Se viene rilevata una sottostringa del form \[ *PropertyName* \] , viene sostituita dal valore della proprietà. Se *PropertyName* non è un nome di proprietà valido, la sottostringa viene risolta come blank. Ad esempio, la colonna Description della [tabella LaunchCondition](launchcondition-table.md) accetta una stringa formattata. Se ERRORTXT è stato impostato su "contattare il personale di supporto". il testo visualizzato per la mancata esecuzione della condizione di avvio includerà quindi questa stringa. Se ERRORTXT non è impostato, il testo visualizzato per la mancata esecuzione della condizione di avvio è semplicemente "sistema non soddisfa i requisiti di installazione".

    

    | Condizione | Descrizione                                                  |
    |-----------|--------------------------------------------------------------|
    | Version9X | Il sistema non soddisfa i requisiti di installazione. \[ERRORTXT\] |

    

     

-   È possibile iterare le parentesi quadre e i nomi delle proprietà vengono risolti dall'interno. Si supponga, ad esempio, che la proprietà della sottostringa \[ \[ \] \] venga visualizzata nel testo. In primo luogo, viene recuperato il valore della proprietà Property a. Se il valore è un nome di proprietà valido, ad esempio PropertyB, viene recuperato il valore di PropertyB e l'intera proprietà della sottostringa \[ \[ \] \] viene sostituita con il valore di PropertyB. Se PropertyA non è un nome di proprietà valido o se il valore di PropertyA non è un nome di proprietà valido, la sottostringa è vuota.
-   Se viene trovata una sottostringa del form \[ % *Metodo EnvironmentVariable* \] , il valore della variabile di ambiente viene sostituito con la sottostringa.
-   Se viene trovata una sottostringa nel formato \[ \\ *x* \] , viene sostituita dal carattere *x* , dove *x* è un carattere, senza ulteriori elaborazioni. Viene mantenuto solo il primo carattere dopo la barra rovesciata; tutte le altre operazioni vengono rimosse. Per includere, ad esempio, una parentesi quadra aperta ( \[ ), usare \[ \\ \[ \] . Il testo della \[ \\ \[ \] parentesi di testo viene \[ \\ \] \] risolto in \[ testo tra parentesi quadre \] .
-   Se una sottostringa è racchiusa tra parentesi graffe ({}) e non contiene nomi di proprietà racchiusi tra parentesi quadre ( \[ \] ), la sottostringa rimane invariata, incluse le parentesi graffe.
-   Se una sottostringa è racchiusa tra parentesi graffe ({}) e contiene uno o più nomi di proprietà racchiusi tra parentesi quadre ( \[ \] ), se tutti i nomi delle proprietà sono validi, il testo (con le sostituzioni risolte) viene visualizzato senza le parentesi graffe.
-   Se viene trovata una sottostringa del form \[ ~ \] , questa viene sostituita con il carattere null. Viene utilizzato per creare stringhe di caratteri reg a più **\_ \_ SZ** nella [tabella del registro di sistema](registry-table.md). Si noti che \[ ~ \] viene usato anche per accodare o anteporre i valori alle variabili di ambiente usando la [tabella dell'ambiente](environment-table.md).
-   Se viene trovata una sottostringa del modulo \[ \# *FileKey* \] , questa viene sostituita dal percorso completo del file, con il valore *FileKey* usato come chiave nella [tabella file](file-table.md). Il valore di \[ \# *FileKey* \] rimane vuoto e non viene sostituito da un percorso fino a quando il programma di installazione non esegue l'azione [CostInitialize](costinitialize-action.md), l' [azione filecost](filecost-action.md)e l' [azione CostFinalize secondo](costfinalize-action.md). Il valore di \[ \# *FileKey* \] dipende dallo stato di installazione del componente a cui appartiene il file. Se il componente viene eseguito dall'origine, il valore è il percorso del percorso di origine del file. Se il componente viene eseguito localmente, il valore è il percorso della posizione di destinazione del file dopo l'installazione. Se il componente presenta uno stato di azione assente, lo stato di installazione del componente viene utilizzato per determinare \[ \) .
-   Se viene trovata una sottostringa del modulo \[ $ *componentkey* \] , questa viene sostituita dalla directory di installazione del componente, con il valore *componentkey* usato come chiave nella tabella dei [componenti](component-table.md). Il valore di \[ $ *componentkey* \] rimane vuoto e non viene sostituito da una directory fino a quando il programma di installazione non esegue l'azione [CostInitialize](costinitialize-action.md), l' [azione filecost](filecost-action.md)e l' [azione CostFinalize secondo](costfinalize-action.md). Il valore di \[ $ *componentkey* \] dipende dallo stato di installazione del componente e dal punto in cui si verifica. Nella colonna valore della tabella del [Registro di sistema](registry-table.md), questa sottostringa può fare riferimento allo stato dell'azione o allo stato dell'azione richiesta del componente. In tutti gli altri casi, questa sottostringa fa riferimento allo stato dell'azione del componente. Se, ad esempio, il componente viene eseguito dall'origine, il valore corrisponde alla directory di origine del file. Se il componente viene eseguito localmente, il valore è la directory di destinazione dopo l'installazione. Se il componente è assente, il valore viene lasciato vuoto. Windows Installer tiene traccia dell'azione e degli Stati di installazione richiesti dei componenti. Ad esempio, se un componente è già installato, potrebbe avere uno stato richiesto locale e uno stato di azione null. Per ulteriori informazioni sul controllo dello stato di installazione dei componenti di, vedere [Verifica dell'installazione di funzionalità, componenti, file](checking-the-installation-of-features-components-files.md).
-   Si noti che se un componente è già installato e non viene reinstallato, rimosso o spostato durante l'installazione corrente, lo stato dell'azione del componente è null e la stringa \[ $ *componentkey* \] restituisce null.
-   Se è presente una sottostringa del form \[ .*FileKey* \] viene sostituito dal percorso completo breve del file, con il valore *FileKey* usato come chiave nella [tabella file](file-table.md).

    Questa sintassi è valida solo se utilizzata nella colonna valore del registro di sistema o nelle tabelle IniFile. Se utilizzata in altre colonne, questa sintassi viene trattata come \[ \# *FileKey* \] .

 

 



