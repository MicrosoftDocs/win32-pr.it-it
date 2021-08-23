---
description: Il tipo di dati Formattato è una stringa di testo elaborata per risolvere nomi di proprietà incorporate, chiavi di tabella, riferimenti a variabili di ambiente e altre sottostringhe speciali.
ms.assetid: 7a1bc160-a06c-4d57-b429-e39167893a45
title: Formattazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c58cd21a53a3f77a646d6da0fac04480bd709ab8f1d7ddcb918d5362a0a366c8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119649642"
---
# <a name="formatted"></a>Formattazione

Il tipo di dati Formattato è una stringa di testo elaborata per risolvere nomi di proprietà incorporate, chiavi di tabella, riferimenti a variabili di ambiente e altre sottostringhe speciali. Per risolvere la stringa vengono riconosciute le convenzioni seguenti:

-   Le parentesi quadre ( ) o le \[ \] parentesi graffe ({ }) senza coppia corrispondente vengono lasciati nel testo.
-   Se viene rilevata una sottostringa del formato \[ *propertyname,* viene sostituita \] dal valore della proprietà . Se *propertyname* non è un nome di proprietà valido, la sottostringa viene risolta come vuota. Ad esempio, la colonna Description della [tabella LaunchCondition](launchcondition-table.md) accetta una stringa formattata. Se ERRORTXT è stato impostato su "Please contact your support personnel". quindi il testo visualizzato per l'esito negativo della condizione di avvio includerà questa stringa. Se ERRORTXT non è impostato, il testo visualizzato per l'esito negativo della condizione di avvio sarà semplicemente "Il sistema non soddisfa i requisiti di installazione".

    

    | Condizione | Descrizione                                                  |
    |-----------|--------------------------------------------------------------|
    | Versione9X | Il sistema non soddisfa i requisiti di installazione. \[ERRORTXT\] |

    

     

-   Le parentesi quadre possono essere iterate e i nomi delle proprietà vengono risolti dall'interno. Si supponga, ad esempio, che nel testo venga visualizzata la \[ \[ sottostringa \] \] PropertyA. In primo luogo, viene recuperato il valore della proprietà PropertyA. Se il valore è un nome di proprietà valido, ad esempio PropertyB, viene recuperato il valore di PropertyB e l'intera sottostringa PropertyA viene sostituita con il \[ \[ valore di \] \] PropertyB. Se PropertyA non è un nome di proprietà valido o se il valore di PropertyA non è un nome di proprietà valido, la sottostringa è vuota.
-   Se viene trovata una sottostringa del formato environmentvariable, il valore della variabile di ambiente \[ %  \] viene sostituito con la sottostringa.
-   Se viene trovata una sottostringa nel formato x, viene sostituita dal carattere x , dove x è un carattere, senza \[ \\  \] ulteriori elaborazioni.   Viene mantenuto solo il primo carattere dopo la barra rovesciata. tutti gli altri elementi vengono rimossi. Ad esempio, per includere una parentesi sinistra letterale ( \[ ), usare \[ \\ \[ \] . Il testo \[ \\ \[ \] Tra \[ \\ \] \] parentesi quadre viene risolto in \[ Testo tra parentesi \] quadre.
-   Se una sottostringa è racchiusa tra parentesi graffe ({ }) e non contiene nomi di proprietà racchiusi tra parentesi quadre ( ), la sottostringa rimane invariata, incluse le parentesi \[ \] graffe.
-   Se una sottostringa è racchiusa tra parentesi graffe ({ }) e contiene uno o più nomi di proprietà racchiusi tra parentesi quadre ( ), se tutti i nomi delle proprietà sono validi, il testo (con le sostituzioni risolte) viene visualizzato senza le parentesi \[ \] graffe.
-   Se viene trovata una sottostringa \[ ~ \] del formato, viene sostituita con il carattere Null. Viene usato per creare stringhe di **caratteri REG MULTI \_ \_ SZ** nella [tabella del Registro di sistema](registry-table.md). Si noti che \[ ~ \] viene usato anche per aggiungere o aggiungere valori di prefisso alle variabili di ambiente usando la [tabella Environment](environment-table.md).
-   Se viene trovata una sottostringa del formato \[ \# *filekey,* viene sostituita dal percorso completo del \] file, [](file-table.md)con il valore *filekey* usato come chiave nella tabella File . Il valore di filekey rimane vuoto e non viene sostituito da un percorso finché il programma di installazione non esegue l'azione \[ \#  \] [CostInitialize](costinitialize-action.md), [l'azione FileCost](filecost-action.md)e [l'azione CostFinalize](costfinalize-action.md). Il valore di \[ \# *filekey* \] dipende dallo stato di installazione del componente a cui appartiene il file. Se il componente viene eseguito dall'origine, il valore è il percorso del percorso di origine del file. Se il componente viene eseguito in locale, il valore è il percorso del percorso di destinazione del file dopo l'installazione. Se lo stato dell'azione del componente è assente, lo stato installato del componente viene usato per determinare \[ \) .
-   Se viene trovata una sottostringa del form \[ $ *componentkey,* viene sostituita dalla \] directory [](component-table.md)di installazione del componente, con il valore *componentkey* usato come chiave nella tabella Component . Il valore di componentkey rimane vuoto e non viene sostituito da una directory finché il programma di installazione non esegue l'azione \[ $  \] [CostInitialize](costinitialize-action.md), [l'azione FileCost](filecost-action.md)e [l'azione CostFinalize](costfinalize-action.md). Il valore di \[ $ *componentkey* \] dipende dallo stato di installazione del componente e dalla posizione in cui si verifica. Nella colonna Valore della tabella del Registro [di](registry-table.md)sistema questa sottostringa può fare riferimento allo stato dell'azione o allo stato dell'azione richiesta del componente. In tutti gli altri casi, questa sottostringa fa riferimento allo stato dell'azione del componente. Ad esempio, se il componente viene eseguito dall'origine, il valore è la directory di origine del file. Se il componente viene eseguito in locale, il valore è la directory di destinazione dopo l'installazione. Se il componente è assente, il valore viene lasciato vuoto. Windows Il programma di installazione tiene traccia sia dell'azione che degli stati di installazione richiesti dei componenti. Ad esempio, se un componente è già installato, potrebbe avere uno stato richiesto locale e uno stato di azione null. Per altre informazioni sul controllo dello stato di installazione dei componenti, vedere [Controllo dell'installazione di funzionalità, componenti, file](checking-the-installation-of-features-components-files.md).
-   Si noti che se un componente è già installato e non viene reinstallato, rimosso o spostato durante l'installazione corrente, lo stato dell'azione del componente è Null e la stringa componentkey restituisce \[ $  \] Null.
-   Se una sottostringa nel formato \[ !*filekey* viene trovato, viene sostituito dal percorso breve completo del file, con il valore filekey usato come chiave \] nella tabella [File](file-table.md). 

    Questa sintassi è valida solo se usata nella colonna Valore del Registro di sistema o nelle tabelle IniFile. Se usata in altre colonne, questa sintassi viene considerata uguale a \[ \# *filekey* \] .

 

 



