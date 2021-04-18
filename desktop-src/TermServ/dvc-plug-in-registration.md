---
title: Registrazione del plug-in DVC
description: Viene descritta la sintassi per la voce del plug-in Dynamic Virtual Channel (DVC) per il client Connessione Desktop remoto (RDC).
ms.assetid: cda4f8c9-867a-41ac-894a-4296d5912b2b
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 183c73f5f9dda0321640119b2750776d207973cc
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "106300298"
---
# <a name="dvc-plug-in-registration"></a>Registrazione del plug-in DVC

Il plug-in Dynamic Virtual Channel (DVC) è registrato per l'utilizzo da parte del client di Connessione Desktop remoto (RDC) utilizzando uno dei metodi seguenti:

-   Viene richiamato il metodo [**IMsTscAdvancedSettings::p UT \_ PluginDlls**](imstscadvancedsettings-plugindlls.md) del controllo ActiveX Remote Desktop Protocol (RDP). Più voci devono essere separate da virgole.
-   Scrittura della voce di plug-in nel seguente percorso del registro di sistema nel computer in cui viene avviato il processo client di Connessione Desktop remoto (RDC):

    **HKEY \_ Software \_ utente corrente** \\  \\ **Microsoft** \\ **Terminal Server** il \\  \\  \\ ***nome del plug-in componenti aggiuntivi predefiniti del*** client Microsoft

    > [!Note]  
    > È necessario creare la sottochiave *univoca del nome del plug-in* se non esiste. Il nome della sottochiave del *nome del plug-in univoco* è una stringa arbitraria che può identificare il plug-in. La stringa può essere costituita da qualsiasi combinazione di caratteri.

     

    In *nome plug-in univoco* è necessario aggiungere una voce che identifichi il plug-in.

    Nome voce = **nome**

    Tipo di dati = **reg \_ SZ** o **reg \_ expand \_ SZ**

In entrambi i casi, il valore della voce deve essere conforme a uno dei formati seguenti:

<dl> <dt>

<span id="Plug-inDLLName__CLSID_"></span><span id="plug-indllname__clsid_"></span><span id="PLUG-INDLLNAME__CLSID_"></span>"*Plug-inDLLName*: {*CLSID*}"
</dt> <dd>

Il plug-in non è necessariamente registrato nel registro di sistema di Windows come oggetto Component Object Model (COM), ma la DLL viene implementata come oggetto COM in-process. Il client RDC caricherà la DLL specificata da *plug-inDLLName* e recupererà l'oggetto com direttamente usando *CLSID*.

</dd> <dt>

<span id="Plug-inDLLName"></span><span id="plug-indllname"></span><span id="PLUG-INDLLNAME"></span>"*Plug-inDLLName*"
</dt> <dd>

La DLL implementa la funzione [**VirtualChannelGetInstance**](virtualchannelgetinstance.md) e la Esporta in base al nome. Il client RDC utilizzerà la funzione **VirtualChannelGetInstance** per ottenere i puntatori dell'interfaccia [**IWTSPlugin**](/windows/desktop/api/TsVirtualChannels/nn-tsvirtualchannels-iwtsplugin) per tutti i plug-in implementati dalla dll.

</dd> <dt>

<span id="_CLSID_"></span><span id="_clsid_"></span>"{*CLSID*}"
</dt> <dd>

Il client RDC creerà un'istanza del plug-in come un normale oggetto COM utilizzando [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) con il *CLSID*.

</dd> </dl>

> [!Note]  
> Il *plug-inDLLName* rappresenta il percorso completo e il nome file del file con estensione dll. Se il tipo di dati è **reg \_ expand \_ SZ**, il percorso può contenere variabili di ambiente non espanse che vengono espanse in fase di esecuzione.

 

Al termine dell'inizializzazione, il client di Connessione Desktop remoto (RDC) eseguirà le operazioni seguenti per ogni plug-in registrato:

1.  Ottenere un'istanza dell'interfaccia [**IWTSPlugin**](/windows/desktop/api/TsVirtualChannels/nn-tsvirtualchannels-iwtsplugin) per ogni plug-in utilizzando uno dei metodi descritti in precedenza.
2.  Chiamare il metodo [**Initialize**](/windows/desktop/api/TsVirtualChannels/nf-tsvirtualchannels-iwtsplugin-initialize) di ogni interfaccia [**IWTSPlugin**](/windows/desktop/api/TsVirtualChannels/nn-tsvirtualchannels-iwtsplugin) .
3.  Se il client si connette più volte allo stesso o a un server diverso, è possibile che siano presenti più chiamate ai metodi [**connessi**](/windows/desktop/api/TsVirtualChannels/nf-tsvirtualchannels-iwtsplugin-connected) e [**disconnessi**](/windows/desktop/api/TsVirtualChannels/nf-tsvirtualchannels-iwtsplugin-disconnected) .
4.  L'ultima chiamata che il plug-in deve gestire viene [**terminata**](/windows/desktop/api/TsVirtualChannels/nf-tsvirtualchannels-iwtsplugin-terminated). È un segnale che il client di Connessione Desktop remoto (RDC) sta per scaricare il plug-in.

 

 