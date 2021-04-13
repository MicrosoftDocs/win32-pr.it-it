---
title: Aggiornamenti alla procedura guidata plug-in DSP per Windows Media Player 11
description: Aggiornamenti alla procedura guidata plug-in DSP per Windows Media Player 11
ms.assetid: 975c18d5-06d7-4db2-a558-bc6557963425
keywords:
- Plug-in di Windows Media Player, creazione guidata plug-in
- plug-in, creazione guidata plug-in
- plug-in di elaborazione dei segnali digitali, creazione guidata plug-in
- Plug-in DSP, creazione guidata plug-in
- procedura guidata plug-in
- Visual Studio, creazione guidata plug-in DSP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0a8efe798a3c324f9ecfac0a5b6021db4ea5abdf
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/19/2020
ms.locfileid: "104398583"
---
# <a name="updates-to-the-dsp-plug-in-wizard-for-windows-media-player-11"></a>Aggiornamenti alla procedura guidata plug-in DSP per Windows Media Player 11

Windows Media Player 11 SDK introduce le seguenti modifiche alla procedura guidata plug-in di DSP:

-   I plug-in registrano il modello di threading come "both". Questo consente l'esecuzione del plug-in nella pipeline Media Foundation in Windows Vista. Vedere il file *NomeProgetto*. RGS.

    -   I plug-in audio DSP hanno il supporto per i due formati aggiuntivi seguenti:

    <!-- -->

    -   \_formato Wave \_ IEEE \_ float
    -   \_Formato Wave \_ estendibile con subformat KSDATAFORMAT \_ sottotipo \_ IEEE \_ float.

    Vedere il file *NomeProgetto*. cpp.

    1.  I plug-in video DSP hanno il supporto per il formato video NV12.
    2.  I plug-in effettuano chiamate aggiuntive a [IWMPMediaPluginRegistrar:: WMPRegisterPlayerPlugin](/previous-versions/windows/desktop/api/wmpservices/nf-wmpservices-iwmpmediapluginregistrar-wmpregisterplayerplugin) e [IWMPMediaPluginRegistrar:: WMPUnRegisterPlayerPlugin](/previous-versions/windows/desktop/api/wmpservices/nf-wmpservices-iwmpmediapluginregistrar-wmpunregisterplayerplugin) con un nuovo tipo di plug-in: WMP \_ plug- \_ DSP \_ OUTOFPROC. Vedere il file *projectnamedll*. cpp del progetto.
    3.  Un progetto aggiuntivo in ogni soluzione crea una DLL proxy/stub per l'interfaccia personalizzata delle impostazioni della pagina delle proprietà. Vedere il progetto *projectnamePS* .
    4.  Le chiamate ai metodi deprecati sono state modificate in modo da usare le versioni più recenti.
    5.  La procedura guidata può generare un plug-in dual mode che funziona sia come DMO, implementando **IMediaObject** e come MFT, implementando **IMFTransform**.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Procedura guidata plug-in DSP**](dsp-plug-in-wizard.md)
</dt> </dl>

 

 




