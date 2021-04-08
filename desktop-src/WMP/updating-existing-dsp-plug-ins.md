---
title: Aggiornamento di plug-in DSP esistenti
description: Aggiornamento di plug-in DSP esistenti
ms.assetid: 0525030e-eb30-41a0-8191-4a5727736857
keywords:
- Plug-in di Windows Media Player, elaborazione dei segnali digitali (DSP)
- plug-in, elaborazione di segnali digitali (DSP)
- plug-in per l'elaborazione di segnali digitali, aggiornamento
- Plug-in DSP, aggiornamento
- versioni di Windows Media Player, plug-in DSP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 393cde356e0d86bb920825e731bb12ee0b7c2818
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/19/2020
ms.locfileid: "103723471"
---
# <a name="updating-existing-dsp-plug-ins"></a>Aggiornamento di plug-in DSP esistenti

I plug-in DSP creati prima del rilascio di Windows Media Player 11 SDK potrebbero non funzionare come previsto con Windows Media Player 11 in esecuzione in Windows Vista. Per assicurarsi che i clienti che eseguono Windows Media Player 11 in Windows Vista possano usare i plug-in, è necessario apportare alcune modifiche al codice del plug-in DSP, ricompilare il progetto e distribuire il plug-in aggiornato ai clienti.

I progetti creati utilizzando la versione più recente della creazione guidata plug-in di Windows Media Player conterranno gli aggiornamenti necessari. Vedere [gli aggiornamenti alla procedura guidata plug-in DSP per Windows Media Player 11](updates-to-the-dsp-plug-in-wizard-for-windows-media-player-11.md). È consigliabile eseguire la procedura guidata per creare un nuovo progetto di esempio e quindi usare uno strumento come Windiff.exe, disponibile in Visual Studio, per esaminare le differenze tra il codice di esempio e il codice di produzione.

È necessario apportare tre modifiche principali a tutti i plug-in DSP esistenti:

-   Modificare il modo in cui viene registrato il plug-in. Il plug-in esistente registra probabilmente il modello di threading come "Apartment". Windows Media Player 11 in esecuzione su Windows Vista richiede che i plug-in DSP registrino il modello di threading come "both". È possibile risolvere il problema modificando il valore del modello di threading nel file *NomeProgetto*. RGS, come indicato di seguito:

    ```C++
    val ThreadingModel = s 'Both'
    
    ```

    

    > [!Note]  
    > Se si specifica il modello di threading come "both", vengono rimosse tutte le serializzazioni fornite da COM per le chiamate alle interfacce personalizzate. Se si effettuano chiamate alle interfacce personalizzate da più thread, è necessario fornire questa serializzazione manualmente.

     

    Windows Media Player 11 garantisce che le chiamate alle interfacce DMO vengano serializzate correttamente.

    1.  Aggiungere chiamate a [IWMPMediaPluginRegistrar:: WMPRegisterPlayerPlugin](/previous-versions/windows/desktop/api/wmpservices/nf-wmpservices-iwmpmediapluginregistrar-wmpregisterplayerplugin) e [IWMPMediaPluginRegistrar:: WMPUnRegisterPlayerPlugin](/previous-versions/windows/desktop/api/wmpservices/nf-wmpservices-iwmpmediapluginregistrar-wmpunregisterplayerplugin) con un nuovo tipo di plug-in: WMP \_ plug- \_ DSP OUTOFPROC \_ in DllRegisterServer e DllUnregisterServer nel file *projectnamedll*. cpp. Per informazioni dettagliate, vedere le pagine di riferimento per questi metodi.
    2.  Creare e distribuire una DLL proxy/stub per abilitare il marshalling COM di qualsiasi interfaccia personalizzata implementata o creata dalla classe del plug-in. Un'interfaccia personalizzata è un'interfaccia proprietaria che è possibile definire e implementare per l'utilizzo da parte dell'oggetto plug-in. Questo include l'interfaccia personalizzata usata dalla pagina delle proprietà, se ne è stato fornito uno, ma potrebbe includere anche interfacce che si connettono ai plug-in dell'interfaccia utente, ad esempio. Un esempio di interfaccia personalizzata creata dalla procedura guidata plug-in è *Iprojectname*. Esempi di interfacce che non sono interfacce personalizzate includono **IMediaObject** e **IWMPPluginEnable**.

Se il plug-in DSP elabora audio, è necessario aggiungere anche il supporto per i nuovi formati audio seguenti:

-   \_formato Wave \_ IEEE \_ float
-   \_Formato Wave \_ estendibile con subformat KSDATAFORMAT \_ sottotipo \_ IEEE \_ float.

Se il plug-in DSP elabora video, è necessario aggiungere il supporto per il formato video NV12.

Vedere il plug-in di esempio audio o video DSP creato dalla procedura guidata per un esempio di come elaborare questi tipi di formato.

## <a name="about-the-proxystub-project"></a>Informazioni sul progetto proxy/stub

Probabilmente il modo più semplice per creare un progetto DLL proxy/stub per il plug-in DSP consiste nell'eseguire la procedura guidata plug-in DSP. Verrà creato un progetto proxy/stub di esempio che è possibile modificare per usare il codice esistente. Sarà necessario apportare le modifiche seguenti:

1.  Rimuovere tutte le definizioni esistenti per le interfacce personalizzate dal codice. Ad esempio, la procedura guidata plug-in DSP di Windows Media Player 10 SDK ha creato la definizione dell'interfaccia *Iprojectname* nel file *NomeProgetto*. h usando la parola chiave **Interface** .
2.  Definire le interfacce personalizzate nel file IDL del progetto di proxy/stub.
3.  Compilare il progetto proxy/stub prima del progetto principale. È possibile configurare Visual Studio in modo che esegua questa operazione automaticamente se entrambi i progetti fanno parte della stessa soluzione.
4.  Il compilatore MIDL creerà un nuovo file di intestazione con un nome nel formato *NomeProgetto* \_ h.h. È necessario includere questa intestazione nel progetto principale (in *NomeProgetto*. h). Contiene le definizioni per le interfacce personalizzate.

## <a name="distributing-the-updated-plug-in"></a>Distribuzione del plug-in aggiornato

È possibile installare il plug-in aggiornato nei computer degli utenti esattamente come in passato. Tuttavia, è ora necessario distribuire e registrare anche la DLL proxy/stub.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Panoramica per gli sviluppatori di plug-in DSP**](dsp-plug-in-developer-overview.md)
</dt> </dl>

 

 




