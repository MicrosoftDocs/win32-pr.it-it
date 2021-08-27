---
title: Aggiornamento dei plug-in DSP esistenti
description: Aggiornamento dei plug-in DSP esistenti
ms.assetid: 0525030e-eb30-41a0-8191-4a5727736857
keywords:
- Windows Media Player plug-in, DSP (Digital Signal Processing)
- plug-in, elaborazione del segnale digitale (DSP)
- plug-in di elaborazione del segnale digitale, aggiornamento
- plug-in DSP, aggiornamento
- versioni di Windows Media Player,plug-in DSP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 725a7a752206f4d321af9deb106df82c40b677dd719182660c5940cac4788244
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120122731"
---
# <a name="updating-existing-dsp-plug-ins"></a>Aggiornamento dei plug-in DSP esistenti

I plug-in DSP creati prima del rilascio di Windows Media Player 11 SDK potrebbero non funzionare come previsto con Windows Media Player 11 in esecuzione in Windows Vista. Per assicurarsi che i clienti che eseguono Windows Media Player 11 in Windows Vista possano usare i plug-in, è necessario apportare alcune modifiche al codice del plug-in DSP, ricompilare il progetto e distribuire il plug-in aggiornato ai clienti.

I progetti creati usando la versione più recente della Windows Media Player guidata plug-in conterranno gli aggiornamenti necessari. Vedere [Aggiornamenti della Creazione guidata plug-in DSP per Windows Media Player 11.](updates-to-the-dsp-plug-in-wizard-for-windows-media-player-11.md) È buona idea eseguire la procedura guidata per creare un nuovo progetto di esempio e quindi usare uno strumento come Windiff.exe, fornito con Visual Studio, per esaminare le differenze tra il codice di esempio e il codice di produzione.

È necessario apportare tre modifiche principali a tutti i plug-in DSP esistenti:

-   Modificare la modalità di registrazione del plug-in. Il plug-in esistente probabilmente registra il modello di threading come "Apartment". Windows Media Player 11 in esecuzione Windows Vista richiede che i plug-in DSP registrino il modello di threading come "Entrambi". È possibile risolvere questo problema modificando il valore del modello di threading nel file *projectname* con estensione rgs, come indicato di seguito:

    ```C++
    val ThreadingModel = s 'Both'
    
    ```

    

    > [!Note]  
    > Se si specifica il modello di threading come "Both", viene rimossa qualsiasi serializzazione fornita da COM per le chiamate alle interfacce personalizzate. Se si effettuano chiamate alle interfacce personalizzate da più thread, è necessario fornire manualmente questa serializzazione.

     

    Windows Media Player 11 garantisce che le chiamate DMO interfacce siano serializzate correttamente.

    1.  Aggiungere chiamate a [IWMPMediaPluginRegistrar::WMPRegisterPlayerPlugin](/previous-versions/windows/desktop/api/wmpservices/nf-wmpservices-iwmpmediapluginregistrar-wmpregisterplayerplugin) e [IWMPMediaPluginRegistrar::WMPUnRegisterPlayerPlugin](/previous-versions/windows/desktop/api/wmpservices/nf-wmpservices-iwmpmediapluginregistrar-wmpunregisterplayerplugin) con un nuovo tipo di plug-in: WMP \_ PLUGINTYPE \_ DSP \_ OUTOFPROC in DllRegisterServer e DllUnregisterServer nel file con estensione cpp nomeprogetto.  Per informazioni dettagliate, vedere le pagine di riferimento per questi metodi.
    2.  Creare e distribuire una DLL proxy/stub per abilitare il marshalling COM di qualsiasi interfaccia personalizzata implementata o creata dalla classe plug-in. Un'interfaccia personalizzata è qualsiasi interfaccia proprietaria definita e implementata per l'uso da parte dell'oggetto plug-in. Ciò include l'interfaccia personalizzata usata dalla pagina delle proprietà, se disponibile, ma potrebbe includere anche interfacce che si connettono ai plug-in dell'interfaccia utente, ad esempio. Un esempio di interfaccia personalizzata creata dalla procedura guidata del plug-in è *Iprojectname*. Esempi di interfacce che non sono interfacce personalizzate includono **IMediaObject** e **IWMPPluginEnable.**

Se il plug-in DSP elabora l'audio, è necessario aggiungere anche il supporto per i nuovi formati audio seguenti:

-   FORMATO \_ WAVE \_ IEEE \_ FLOAT
-   WAVE \_ FORMAT \_ EXTENSIBLE con sottoformato KSDATAFORMAT \_ SUBTYPE \_ IEEE \_ FLOAT.

Se il plug-in DSP elabora i video, è necessario aggiungere il supporto per il formato video NV12.

Per un esempio di come elaborare questi tipi di formato, vedere il plug-in DSP audio o video di esempio creato dalla procedura guidata.

## <a name="about-the-proxystub-project"></a>Informazioni sul proxy/stub Project

Probabilmente il modo più semplice per creare un progetto dll proxy/stub per il plug-in DSP è eseguire la procedura guidata del plug-in DSP. Verrà creato un progetto proxy/stub di esempio che è possibile modificare per usare il codice esistente. Sarà necessario apportare le modifiche seguenti:

1.  Rimuovere eventuali definizioni esistenti per le interfacce personalizzate dal codice. Ad esempio, la procedura guidata del plug-in DSP dell'SDK Windows Media Player 10 ha creato la definizione dell'interfaccia *Iprojectname* nel file nomeprogetto *con* estensione h usando la parola chiave **interface.**
2.  Definire le interfacce personalizzate nel file IDL del progetto proxy/stub.
3.  Compilare il progetto proxy/stub prima del progetto principale. È possibile configurare Visual Studio questa operazione automaticamente se entrambi i progetti fanno parte della stessa soluzione.
4.  Il compilatore MIDL creerà un nuovo file di intestazione con un nome nel *formato nomeprogetto* \_ h.h. È necessario includere questa intestazione nel progetto principale (in *nomeprogetto*.h). Contiene le definizioni per le interfacce personalizzate.

## <a name="distributing-the-updated-plug-in"></a>Distribuzione del plug-in aggiornato

È possibile installare il plug-in aggiornato nei computer degli utenti esattamente come in passato. Tuttavia, è ora necessario distribuire e registrare anche la DLL proxy/stub.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Panoramica per gli sviluppatori di plug-in DSP**](dsp-plug-in-developer-overview.md)
</dt> </dl>

 

 




