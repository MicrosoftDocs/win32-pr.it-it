---
title: Riconfigurazione della barra multifunzione con le modalità applicazione
description: Il Framework della barra multifunzione di Windows supporta la riconfigurazione dinamica e l'esposizione degli elementi principali dell'interfaccia utente della barra multifunzione in fase di esecuzione, in base allo stato dell'applicazione (noto anche come contesto).
ms.assetid: 8e9d85c5-33e4-4212-b9e4-2fc3b492c273
keywords:
- Barra multifunzione di Windows, riconfigurazione con modalità applicazione
- Barra multifunzione, riconfigurazione con modalità applicazione
- riconfigurazione della barra multifunzione di Windows con modalità applicazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 83d206c238e6fe7463562077daaa52a5522a79d9
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104399042"
---
# <a name="reconfiguring-the-ribbon-with-application-modes"></a>Riconfigurazione della barra multifunzione con le modalità applicazione

Il Framework della barra multifunzione di Windows supporta la riconfigurazione dinamica e l'esposizione degli elementi principali dell'interfaccia utente della barra multifunzione in fase di esecuzione, in base allo stato dell'applicazione (noto anche come contesto). Dichiarati e associati a elementi specifici nel markup, i vari stati supportati da un'applicazione sono definiti modalità applicazione.

-   [Introduzione](#introduction)
-   [Interfaccia utente contestuale](#contextual-user-interface)
    -   [Uno scenario semplice in modalità applicazione](#a-simple-application-mode-scenario)
-   [Implementazione di modalità applicazione](#implementing-application-modes)
    -   [Identificare le modalità](#identify-the-modes)
    -   [Assegnare controlli alle modalità applicazione](#assign-controls-to-application-modes)
    -   [Modalità switch in fase di esecuzione](#switch-modes-at-runtime)
-   [Osservazioni:](#remarks)
-   [Argomenti correlati](#related-topics)

## <a name="introduction"></a>Introduzione

Le modalità applicazione sono costituite da gruppi logici di controlli che espongono alcune funzionalità principali dell'applicazione nell'interfaccia utente della barra multifunzione. Queste modalità sono abilitate o disabilitate in modo dinamico dall'applicazione tramite una chiamata al metodo del Framework [**IUIFramework:: Semodes**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setmodes), che attiva o disattiva la visibilità di una o più modalità di applicazione.

## <a name="contextual-user-interface"></a>Interfaccia utente contestuale

Il Framework della barra multifunzione offre un'esperienza utente avanzata incorporando controlli dinamici che rispondono facilmente all'interazione dell'utente e al contesto dell'applicazione. Questa ricca interfaccia utente contestuale viene fornita tramite una combinazione dei meccanismi seguenti:

-   Raccolte: controlli basati su raccolte che supportano la manipolazione dinamica delle raccolte di elementi.
-   Schede contestuali: schede della barra multifunzione con visibilità determinata da una modifica nel contesto dell'area di lavoro, ad esempio la selezione di un'immagine in un documento.
-   Modalità applicazione: funzionalità dell'applicazione principale che dipende dal contesto dell'applicazione.

In alcuni casi, le modalità di applicazione sono apparentemente simili alle schede contestuali. Tuttavia, la distinzione fondamentale risiede nello scopo e nell'ambito di ciascuna di esse.

I controlli contestuali vengono attivati in risposta a una modifica del contesto all'interno di un'applicazione. Ad esempio, in Microsoft Paint per Windows 7, una scheda contestuale contenente gruppi di comandi correlati al testo viene visualizzata quando un utente inserisce un'area di testo nell'area di lavoro. Questa scheda contestuale non contiene i comandi di base per l'applicazione ed è esposta solo nell'interfaccia utente perché il contesto *all'interno* dell'applicazione è stato modificato. La funzionalità di base dell'applicazione, ovvero i comandi per la modifica di immagini, è ancora pertinente e disponibile per l'utente, anche con la scheda contestuale visibile.

Le modalità di applicazione sono diverse dai controlli contestuali perché riconfigurano le funzionalità in risposta alle modifiche nel contesto in cui l'applicazione sta operando. Le modalità dell'applicazione si trovano a un livello superiore di astrazione; consentono di riconfigurare la funzionalità di base di un'applicazione anziché esporre temporaneamente la funzionalità che non è un componente principale dell'interfaccia utente. Ad esempio, in Microsoft Paint per Windows 7, un'opzione in modalità applicazione si verifica quando viene richiamato il comando **Anteprima di stampa** . Quando Microsoft Paint passa all' **Anteprima di stampa**, il contesto in cui l'applicazione sta operando passa dalla modifica alla visualizzazione in anteprima. Di conseguenza, le funzionalità principali dell'applicazione cambiano fino a quando l' **Anteprima di stampa** non viene annullata e l'applicazione entra nuovamente nel contesto di modifica.

### <a name="a-simple-application-mode-scenario"></a>Uno scenario semplice in modalità applicazione

Nello scenario seguente viene illustrato come vengono utilizzate le modalità applicazione, in un'applicazione denominata RibbonApp, per esporre aspetti discreti della funzionalità di base.

In RibbonApp sono definite due modalità di applicazione:

-   La modalità **semplice** espone i comandi di base nell'interfaccia utente della barra multifunzione. Questi comandi vengono visualizzati sempre, indipendentemente dalla modalità di applicazione attiva.
-   La modalità **avanzata** espone comandi complessi destinati a utenti esperti dell'applicazione. Questi comandi avanzati vengono visualizzati nell'interfaccia utente della barra multifunzione, oltre ai semplici comandi.

Per impostazione predefinita, RibbonApp è impostato per l'apertura in modalità **semplice** e i comandi richiesti dagli utenti esperti vengono visualizzati nel **menu applicazione** e nella scheda **Home** . Le schermate seguenti mostrano il **menu dell'applicazione** RibbonApp e la scheda **Home** in modalità **semplice** , evidenziando i controlli modali.

![screenshot che mostra una scheda per la modalità applicazione semplice.](images/overviews/appmode-hometab.png)![screenshot che mostra il menu applicazione per la modalità applicazione semplice.](images/overviews/appmode-simpleappmenu.png)

Sebbene questi comandi siano sufficienti per gli utenti principianti, RibbonApp supporta anche gli utenti esperti tramite una modalità **avanzata** che, quando attivata, facendo clic sul pulsante **passa a modalità avanzata** nel **menu applicazione**, Visualizza funzionalità principali aggiuntive.

Questo scenario viene facilmente implementato associando vari elementi nel markup a modalità di applicazione discrete che possono essere attivate e disattivate in base alle esigenze. Le schermate seguenti mostrano il **menu dell'applicazione** RibbonApp e la scheda **Home** in modalità **avanzata** , evidenziando i controlli modali.

![screenshot che mostra una scheda per la modalità di applicazione avanzata.](images/overviews/appmode-advancedtab.png)![screenshot che mostra il menu dell'applicazione per la modalità di applicazione avanzata.](images/overviews/appmode-advancedappmenu.png)

## <a name="implementing-application-modes"></a>Implementazione di modalità applicazione

In questa sezione vengono illustrati i tre passaggi necessari per l'implementazione delle modalità applicazione della barra multifunzione. RibbonApp viene usato per fornire un esempio per ogni passaggio.

### <a name="identify-the-modes"></a>Identificare le modalità

Ogni modalità in un'applicazione deve rappresentare un set logico di funzionalità che dipende dal contesto in cui un'applicazione è in grado di operare. Se, ad esempio, in un'applicazione vengono visualizzati i controlli rilevanti solo quando viene rilevata una connessione di rete, tali controlli operano all'interno di un contesto di rete che potrebbe giustificare la creazione di una modalità di **rete** .

In RibbonApp sono disponibili due contesti che possono essere attivi in un determinato momento, ovvero **semplici** e **avanzati**. RibbonApp richiede quindi due modalità: **semplice** e **avanzata**.

### <a name="assign-controls-to-application-modes"></a>Assegnare controlli alle modalità applicazione

Una volta identificate le modalità dell'applicazione, assegnare ogni controllo Ribbon a una modalità dichiarando un attributo *ApplicationModes* nel markup per gli elementi di controllo che supportano le modalità di applicazione.

La visualizzazione della barra multifunzione consente di specificare le modalità sugli elementi di controllo seguenti:

-   Elementi principali della [**scheda**](windowsribbon-element-tab.md) .
-   [**Raggruppa**](windowsribbon-element-group.md) gli elementi figlio di un elemento [**scheda**](windowsribbon-element-tab.md) principale.
-   Elementi [**Button**](windowsribbon-element-button.md), [**SplitButton**](windowsribbon-element-splitbutton.md)e [**DropDownButton**](windowsribbon-element-dropdownbutton.md) assegnati a un [**MenuGroup**](windowsribbon-element-menugroup.md) nel [menu dell'applicazione](windowsribbon-controls-applicationmenu.md).
    > [!Note]  
    > Gli elementi [**Button**](windowsribbon-element-button.md), [**SplitButton**](windowsribbon-element-splitbutton.md)e [**DropDownButton**](windowsribbon-element-dropdownbutton.md) non possono essere assegnati a una modalità a meno che non siano ospitati nel [menu dell'applicazione](windowsribbon-controls-applicationmenu.md).

     

Nel framework della barra multifunzione questi elementi di controllo sono detti controlli modali. Vengono visualizzati solo se una modalità a cui sono associati è attiva nell'interfaccia utente.

Gli elementi del controllo contenuti in un controllo modale ereditano il comportamento della modalità di applicazione. Se, ad esempio, un controllo modale del [**gruppo**](windowsribbon-element-group.md) viene assegnato a una modalità **avanzata** e la modalità **avanzata** non è attiva, il **gruppo** e gli eventuali controlli, modale o altro, non saranno visibili nell'interfaccia utente della barra multifunzione.

Con l'uso dell'attributo *ApplicationModes* , le modalità vengono assegnate ai controlli modali in una relazione 1: N (uno-a-molti), in cui un singolo controllo modale può essere associato a più modalità.

Il Framework della barra multifunzione fa riferimento alle modalità numeriche, da 0 a 31, con la modalità 0 considerata la modalità predefinita attivata automaticamente all'avvio di un'applicazione barra multifunzione. Qualsiasi controllo modale che non specifica un attributo *ApplicationModes* viene considerato membro della modalità predefinita.

In RibbonApp, **Simple** è la modalità predefinita, con la funzionalità modalità **avanzata** visualizzata solo quando viene avviata dall'utente.

Nell'esempio seguente viene illustrato il markup richiesto per RibbonApp.


```C++
<Application.Views>
  <Ribbon>

    <!--Application Menu-->
    <Ribbon.ApplicationMenu>
      <ApplicationMenu CommandName='cmdAppMenu'>                    
        <MenuGroup>
          <Button CommandName='cmdSave'/>                        
          <Button CommandName='cmdExportMetadata' ApplicationModes='1'/>                   
        </MenuGroup>              
        <MenuGroup>
          <Button CommandName='cmdSwitchModes' ApplicationModes ='0,1'/>
          <Button CommandName='cmdExit'/>
        </MenuGroup>
      </ApplicationMenu>
    </Ribbon.ApplicationMenu>
            
    <!--Tabs-->
    <Ribbon.Tabs>
      <!--Home Tab-->
      <Tab CommandName='cmdHomeTab'>
                    
        <!--Scaling Policy for Home tab-->
        <Tab.ScalingPolicy>
          <ScalingPolicy>
            <ScalingPolicy.IdealSizes>
              <Scale Group='cmdSimpleControlsGroup' Size='Medium'/>                                
            </ScalingPolicy.IdealSizes>                     
          </ScalingPolicy>
        </Tab.ScalingPolicy>     
                    
        <!--Simple Controls Group-->
        <Group CommandName='cmdSimpleControlsGroup' SizeDefinition='ThreeButtons-OneBigAndTwoSmall'>                        
          <Button CommandName="cmdPaste" />
          <Button CommandName='cmdCut'/>                        
          <Button CommandName='cmdCopy'/>                        
        </Group>
      </Tab>
                
      <!--Advanced Tab-->
      <Tab CommandName='cmdAdvancedTab' ApplicationModes='1'>
        <!--Advanced Controls Group-->
        <Group CommandName='cmdMetadataGroup' ApplicationModes='1' SizeDefinition='TwoButtons'>
          <Button CommandName='cmdEditMetadata' />
          <Button CommandName='cmdCheckErrors' />
        </Group>
      </Tab>
    </Ribbon.Tabs>                   
                             
  </Ribbon>         
</Application.Views>
```



In questo esempio viene illustrato quanto segue:

-   Non è necessario dichiarare in modo esplicito la modalità predefinita 0. Poiché i controlli modali che non specificano l'attributo *ApplicationModes* vengono associati automaticamente alla modalità 0 (modalità **semplice** nell'esempio RibbonApp), non è necessario dichiarare in modo esplicito l'attributo per i controlli modali predefiniti.
-   I controlli possono essere associati a più modalità. Per RibbonApp, l'unico elemento necessario per l'attributo *ApplicationModes* in un controllo in modalità **semplice** è il `cmdSwitchModes` pulsante, perché fa parte di entrambe le modalità **semplici** e **Avanzate** . Se una delle due modalità è attiva, questo controllo verrà visualizzato nel [menu dell'applicazione](windowsribbon-controls-applicationmenu.md).
-   I controlli modali non ereditano dagli elementi padre. La scheda **Avanzate** di RibbonApp contiene un gruppo di **metadati** . entrambi i controlli modali sono assegnati alla modalità 1 (modalità **avanzata** ). L'assegnazione della scheda **Avanzate** alla modalità 1 non assegna automaticamente i controlli figlio, ad esempio il gruppo di **metadati** , alla modalità 1. In questo modo, tutti i gruppi all'interno di una scheda possono essere abilitati o disabilitati indipendentemente in fase di esecuzione.
-   I controlli non modale possono continuare a basarsi su commutatori di modalità. I pulsanti **Modifica metadati** e **Controlla errori** di RibbonApp sono per utenti avanzati e sono disponibili solo quando l'utente passa alla modalità **avanzata** . I controlli pulsante che non sono ospitati nel [menu dell'applicazione](windowsribbon-controls-applicationmenu.md) sono non modale; Tuttavia, poiché questi pulsanti sono ospitati all'interno di un controllo modale (il gruppo di **metadati** ), sono visibili quando il gruppo è visibile. Pertanto, questi pulsanti vengono visualizzati quando viene attivata la modalità avanzata e il gruppo di **metadati** viene esposto nell'interfaccia utente della barra multifunzione.

### <a name="switch-modes-at-runtime"></a>Modalità switch in fase di esecuzione

Una volta definite nel markup, le modalità possono essere facilmente abilitate o disabilitate in risposta a eventi contestuali. Come indicato in precedenza, le applicazioni Ribbon vengono sempre avviate nella modalità predefinita 0. Dopo che l'applicazione è stata inizializzata e la modalità 0 è attiva, il set di modalità attive può essere modificato chiamando la funzione [**IUIFramework:: Semodes**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setmodes) . Questa funzione accetta un intero a 32 bit come rappresentazione bit per bit delle modalità che devono essere attive. il bit meno significativo rappresenta la modalità 0 e il bit più significativo rappresenta la modalità 31. Se un bit è impostato su zero, la modalità non è attiva nell'interfaccia utente della barra multifunzione.

In RibbonApp, quando un utente abilita la modalità **avanzata** , i comandi avanzati vengono visualizzati insieme ai semplici comandi. Il gestore di comandi per il pulsante **passa a modalità avanzata** chiama [**IUIFramework:: semodes**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setmodes) per impostare le modalità 0 (**semplice**) e 1 (**avanzata**) come attivo nell'interfaccia utente. Nell'esempio seguente viene riportato il codice RibbonApp per la chiamata di funzione:


```C++
const int SIMPLE_MODE = 0;
const int ADVANCED_MODE = 1;
pFramework->SetModes( UI_MAKEAPPMODE(SIMPLE_MODE) | UI_MAKEAPPMODE(ADVANCED_MODE) );
```



> [!Note]  
> La macro MAKEAPPMODE dell'interfaccia utente del Framework della barra multifunzione \_ semplifica l'impostazione corretta di questi bit in preparazione alla chiamata a [**IUIFramework:: semodes**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setmodes).

 

In questo esempio viene illustrato quanto segue:

-   Usare la macro MAKEAPPMODE dell'interfaccia utente \_ per compilare un set di modalità.
-   Le modalità vengono impostate in modo esplicito e atomico. Il valore integer passato a [**IUIFramework::**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setmodes) sequests rappresenta le modalità che saranno attive dopo la restituzione della funzione. Sebbene la modalità **semplice** fosse precedentemente attiva, **IUIFramework:: semodes** deve indicare che la modalità **semplice** rimane attiva quando viene attivata la modalità **avanzata** .
-   La modalità predefinita può essere rimossa. Sebbene in RibbonApp la modalità predefinita (modalità 0) non venga mai rimossa, è possibile rimuoverla con la chiamata seguente: `g_pFramework->SetModes(UI_MAKEAPPMODE(ADVANCED_MODE))` , esponendo solo i comandi avanzati nell'interfaccia utente.

> [!Note]  
> Quando le modalità di un'applicazione vengono riconfigurate, la barra multifunzione tenterà di mantenere la scheda selezionata in precedenza nell'interfaccia utente. Se il nuovo set di modalità non contiene più la scheda selezionata prima della chiamata, la barra multifunzione selezionerà la scheda nel layout più vicino al [menu dell'applicazione](windowsribbon-controls-applicationmenu.md). Questa scheda è destinata a contenere i comandi più rilevanti per l'utente. Per altre informazioni, vedere [linee guida sull'esperienza utente della barra multifunzione](https://msdn.microsoft.com/library/cc872782.aspx).

 

## <a name="remarks"></a>Commenti

La barra multifunzione deve avere almeno una modalità attiva in qualsiasi momento. Se un'applicazione tenta di disattivare tutte le modalità chiamando [**IUIFramework:: Semodes**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setmodes) con un valore di modalità pari a 0, \_ viene restituito l'errore e il set di modalità attivo rimane invariato.

Il Framework richiede che almeno una scheda sia presente nell'interfaccia utente della barra multifunzione sempre. Di conseguenza, deve essere presente almeno una scheda esposta dalla modalità predefinita (modalità 0) e dopo ogni cambio di modalità.

Non tutte le aree dell'interfaccia utente della barra multifunzione sono interessate dalle modalità di applicazione. Se, ad esempio, la disabilitazione di una modalità causa la scomparsa dei pulsanti della barra multifunzione aggiunti in precedenza alla [barra di accesso rapido](windowsribbon-controls-quickaccesstoolbar.md), tali pulsanti rimarranno nella barra di accesso rapido, consentendo agli utenti di eseguire i comandi associati ai pulsanti. Come regola generale, se un comando appartiene a una o più modalità inattive, è necessario disabilitare anche tale comando impostando la proprietà [UI \_ pkey \_ Enabled](windowsribbon-reference-properties-uipkey-enabled.md) su 0 (variante \_ false).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Linee guida sull'esperienza utente della barra multifunzione](https://msdn.microsoft.com/library/cc872782.aspx)
</dt> <dt>

[Visualizzazione di schede contestuali](ribbon-contextualtabs.md)
</dt> </dl>

 

 