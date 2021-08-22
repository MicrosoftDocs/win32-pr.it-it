---
title: Registrazione del plug-in DVC
description: Viene descritta la sintassi per la voce del plug-in DVC (Dynamic Virtual Channel) per il client Connessione Desktop remoto (RDC).
ms.assetid: cda4f8c9-867a-41ac-894a-4296d5912b2b
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 88d3660b4d9c704c9a59335cede886085f13414991dc2dc913185d407e0a3c54
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119515528"
---
# <a name="dvc-plug-in-registration"></a>Registrazione del plug-in DVC

Il plug-in DVC (Dynamic Virtual Channel) viene registrato per l'uso da parte del client Connessione Desktop remoto (RDC) usando uno dei metodi seguenti:

-   Chiamata del [**metodo IMsTscAdvancedSettings::p ut \_ PluginDlls**](imstscadvancedsettings-plugindlls.md) del controllo Remote Desktop Protocol (RDP) ActiveX. Più voci devono essere separate da virgole.
-   Scrittura della voce del plug-in nel percorso seguente nel Registro di sistema nel computer in cui viene avviato il processo client Connessione Desktop remoto (RDC):

    **HKEY \_ CURRENT \_ USER** \\ **Software** \\ **Microsoft** \\ **Terminal Server Client** Default \\  \\ **AddIns** \\ **_unique plug-in name_**

    > [!Note]  
    > Se non esiste, è necessario creare la sottochiave del nome *del plug-in* univoco. Il *nome univoco della sottochiave del* nome del plug-in è una stringa arbitraria in grado di identificare il plug-in. La stringa può essere qualsiasi combinazione di caratteri.

     

    In *nome plug-in univoco* è necessario aggiungere una voce che identifica il plug-in.

    Nome voce = **Nome**

    Tipo di dati = **REG \_ SZ** o **REG EXPAND \_ \_ SZ**

In entrambi i casi, il valore della voce deve essere conforme a uno dei formati seguenti:

<dl> <dt>

<span id="Plug-inDLLName__CLSID_"></span><span id="plug-indllname__clsid_"></span><span id="PLUG-INDLLNAME__CLSID_"></span>"*Plug-inDLLName*:{*CLSID*}"
</dt> <dd>

Il plug-in non è necessariamente registrato nel registro Windows come oggetto Component Object Model (COM), ma la DLL viene implementata come oggetto COM in-process. Il client RDC carica la DLL specificata da *Plug-inDLLName* e recupera l'oggetto COM direttamente usando *CLSID*.

</dd> <dt>

<span id="Plug-inDLLName"></span><span id="plug-indllname"></span><span id="PLUG-INDLLNAME"></span>"*Plug-inDLLName*"
</dt> <dd>

La DLL implementa la [**funzione VirtualChannelGetInstance**](virtualchannelgetinstance.md) e la esporta in base al nome. Il client RDC userà la **funzione VirtualChannelGetInstance** per ottenere puntatori a interfaccia [**IWTSPlugin**](/windows/desktop/api/TsVirtualChannels/nn-tsvirtualchannels-iwtsplugin) per tutti i plug-in implementati dalla DLL.

</dd> <dt>

<span id="_CLSID_"></span><span id="_clsid_"></span>"{*CLSID*}"
</dt> <dd>

Il client RDC crea un'istanza del plug-in come oggetto COM normale usando [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) con *CLSID*.

</dd> </dl>

> [!Note]  
> *Plug-inDLLName rappresenta* il percorso completo e il nome file del .dll file. Se il tipo di dati **è REG \_ EXPAND \_ SZ**, il percorso può contenere variabili di ambiente non espanse espanse in fase di esecuzione.

 

Quando il client Connessione Desktop remoto (RDC) termina l'inizializzazione, eseguirà le operazioni seguenti per ogni plug-in registrato:

1.  Ottenere un'istanza [**dell'interfaccia IWTSPlugin**](/windows/desktop/api/TsVirtualChannels/nn-tsvirtualchannels-iwtsplugin) per ogni plug-in usando uno dei metodi descritti in precedenza.
2.  Chiamare il [**metodo Initialize**](/windows/desktop/api/TsVirtualChannels/nf-tsvirtualchannels-iwtsplugin-initialize) di ogni [**interfaccia IWTSPlugin.**](/windows/desktop/api/TsVirtualChannels/nn-tsvirtualchannels-iwtsplugin)
3.  Se il client si connette più volte allo stesso server o a un server diverso, è possibile che siano presenti più chiamate ai metodi [**Connected**](/windows/desktop/api/TsVirtualChannels/nf-tsvirtualchannels-iwtsplugin-connected) e [**Disconnected.**](/windows/desktop/api/TsVirtualChannels/nf-tsvirtualchannels-iwtsplugin-disconnected)
4.  L'ultima chiamata che il plug-in deve gestire è [**Terminated.**](/windows/desktop/api/TsVirtualChannels/nf-tsvirtualchannels-iwtsplugin-terminated) È un segnale che il client Connessione Desktop remoto (RDC) sta per scaricare il plug-in.

 

 