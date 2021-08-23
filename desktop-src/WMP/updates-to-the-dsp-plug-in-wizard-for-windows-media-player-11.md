---
title: Aggiornamenti alla Creazione guidata plug-in DSP per Windows Media Player 11
description: Aggiornamenti alla Creazione guidata plug-in DSP per Windows Media Player 11
ms.assetid: 975c18d5-06d7-4db2-a558-bc6557963425
keywords:
- Windows Media Player plug-in, procedura guidata plug-in
- plug-in, procedura guidata plug-in
- plug-in di elaborazione dei segnali digitali, procedura guidata plug-in
- plug-in DSP, procedura guidata plug-in
- Procedura guidata plug-in
- Visual Studio,Procedura guidata plug-in DSP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e2fb6ffaa9384f46e4630b16310a599de8508d953aabd4a5cdf277e91c130641
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119762171"
---
# <a name="updates-to-the-dsp-plug-in-wizard-for-windows-media-player-11"></a>Aggiornamenti alla Creazione guidata plug-in DSP per Windows Media Player 11

L Windows Media Player SDK di Windows Media Player 11 introduce le modifiche seguenti alla procedura guidata del plug-in DSP:

-   I plug-in registrano il modello di threading come "Entrambi". In questo modo il plug-in può essere eseguito nella pipeline Media Foundation in Windows Vista. Vedere il file *projectname* con estensione rgs.

    -   I plug-in DSP audio supportano i due formati aggiuntivi seguenti:

    <!-- -->

    -   FORMATO \_ WAVE \_ IEEE \_ FLOAT
    -   WAVE \_ FORMAT \_ EXTENSIBLE con sottoformato KSDATAFORMAT \_ SUBTYPE \_ IEEE \_ FLOAT.

    Vedere *il* file con estensione cpp nomeprogetto.

    1.  I plug-in DSP video supportano il formato video NV12.
    2.  I plug-in effettuano chiamate aggiuntive a [IWMPMediaPluginRegistrar::WMPRegisterPlayerPlugin](/previous-versions/windows/desktop/api/wmpservices/nf-wmpservices-iwmpmediapluginregistrar-wmpregisterplayerplugin) e [IWMPMediaPluginRegistrar::WMPUnRegisterPlayerPlugin](/previous-versions/windows/desktop/api/wmpservices/nf-wmpservices-iwmpmediapluginregistrar-wmpunregisterplayerplugin) con un nuovo tipo di plug-in: WMP \_ PLUGINTYPE \_ DSP \_ OUTOFPROC. Vedere il file con estensione cpp *projectnamedll* del progetto.
    3.  Un progetto aggiuntivo in ogni soluzione crea una DLL proxy/stub per l'interfaccia personalizzata delle impostazioni della pagina delle proprietà. Vedere il *progetto projectnamePS.*
    4.  Le chiamate ai metodi deprecati sono state modificate per usare le versioni più recenti.
    5.  La procedura guidata può generare un plug-in in modalità doppia che funziona sia come DMO, implementando **IMediaObject** che come MFT, implementando **IMFTransform.**

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Creazione guidata plug-in DSP**](dsp-plug-in-wizard.md)
</dt> </dl>

 

 




