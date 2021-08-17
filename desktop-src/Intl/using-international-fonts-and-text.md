---
description: In ogni versione principale di Windows sono stati aggiunti tipi di carattere per supportare lingue e script internazionali.
ms.assetid: 77b8c200-2682-4651-855a-602f768edc9b
title: Enumerazione e selezione dei caratteri internazionali
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a4b28e2dca3937f3513a930f157a364d466f761ed54a53d09c3e2b8b1c89bb30
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119146884"
---
# <a name="international-font-enumeration-and-selection"></a>Enumerazione e selezione dei caratteri internazionali

In ogni versione principale di Windows sono stati aggiunti tipi di carattere per supportare lingue e script internazionali. Fare riferimento a Supporto di script e tipi di carattere [in Windows](https://msdn.microsoft.com/globalization/mt791278) per i tipi di carattere aggiunti in ogni versione di Windows a partire dal Windows 2000, nonché per gli script, le aree e le lingue supportati.

## <a name="enumfontfamiliesex"></a>EnumFontFamiliesEx

Per enumerare i tipi di carattere internazionali nell'applicazione, è possibile usare la [**funzione EnumFontFamiliesEx.**](/windows/win32/api/wingdi/nf-wingdi-enumfontfamiliesexa) **EnumFontFamiliesEx** consente di enumerare i tipi di carattere in base al nome del carattere tipografico e al set di caratteri passando un puntatore a una struttura [**LOGFONT**](/windows/win32/api/wingdi/ns-wingdi-logfonta) che contiene il nome del carattere tipografico e le informazioni sul set di caratteri. Per chiamare **EnumFontFamiliesEx,** è possibile specificare un nome di carattere tipografico o un set di caratteri oppure è possibile richiedere qualsiasi elemento disponibile. L'impostazione del nome del carattere tipografico **di LOGFONT** su **NULL** enumera tutti i nomi dei caratteri tipografici. L'impostazione del campo charset **su DEFAULT \_ CHARSET** enumera tutti i set di caratteri.

Si noti che i set di caratteri sono una nozione legacy corrispondente ai set di caratteri pre-Unicode. Al momento non esiste alcun meccanismo per enumerare i tipi di carattere che supportano script arbitrari o intervalli di caratteri in Unicode. La struttura [**NEWTEXTMETRICEX**](/windows/win32/api/wingdi/ns-wingdi-newtextmetricexa) passata da [**EnumFontFamExProc**](/previous-versions//dd162618(v=vs.85)) include la struttura [**FONTSIGNATURE,**](/windows/win32/api/wingdi/ns-wingdi-fontsignature) che include dichiarazioni più dettagliate fornite dallo sviluppatore di tipi di carattere per le pagine di codice e gli intervalli Unicode supportati dal tipo di carattere. Per determinare in modo più preciso gli intervalli di caratteri supportati da un determinato tipo di carattere, selezionare il tipo di carattere in un contesto di dispositivo e chiamare [**GetFontUnicodeRanges**](/windows/win32/api/wingdi/nf-wingdi-getfontunicoderanges). Si noti che questa API non supporta i piani supplementari Unicode.

## <a name="choosefont"></a>ChooseFont

È possibile usare la [**funzione ChooseFont**](/previous-versions/windows/desktop/legacy/ms646914(v=vs.85)) per visualizzare una finestra di dialogo comune che consente all'utente di selezionare tipi di carattere internazionali in base al set di caratteri. È possibile specificare uno dei tre flag per determinare, in base al set di caratteri, quali tipi di carattere vengono visualizzati nella finestra di dialogo ChooseFont: **CF \_ SCRIPTSONLY,** **CF \_ SELECTSCRIPT** o **CF \_ NOSCRIPTSEL.**

Il flag **CF \_ SCRIPTSONLY indica** all'API di elencare i tipi di carattere per tutti i set di caratteri che non sono Symbol o OEM.

Se si desidera visualizzare solo i tipi di carattere che coprono un determinato set di caratteri, è necessario specificare il flag **CF \_ SELECTSCRIPT**. Prima di [**chiamare ChooseFont**](/previous-versions/windows/desktop/legacy/ms646914(v=vs.85)), inizializzare il campo *lfCharSet* della [**struttura LOGFONT.**](/windows/win32/api/wingdi/ns-wingdi-logfonta) Se si è interessati a specificare solo il set di caratteri, impostare gli altri campi della struttura **LOGFONT** su **NULL.** Per fare **in modo che ChooseFont** guardi la **struttura LOGFONT,** è necessario specificare anche il flag **CF \_ INITTOLOGFONTSTRUCT.**

Infine, come per qualsiasi altro campo nella finestra di dialogo Tipo di carattere, è possibile scegliere di visualizzare una casella di riepilogo script vuota. Questa funzionalità è utile se l'utente ha evidenziato diversi tipi di carattere che si estendono su diversi set di caratteri. In questo caso, è necessario chiamare [**ChooseFont con**](/previous-versions/windows/desktop/legacy/ms646914(v=vs.85)) il flag **CF \_ NOSCRIPTSEL.**

A partire da Windows 7, [**ChooseFont implementa**](/previous-versions/windows/desktop/legacy/ms646914(v=vs.85)) il supporto per nascondere i tipi di carattere dagli elenchi di selezione dei tipi di carattere. **ChooseFont** elenca solo i tipi di carattere visualizzati e filtra i tipi di carattere nascosti durante la visualizzazione dei tipi di carattere nella casella di riepilogo. Il flag aggiuntivo (**CF \_ INACTIVEFONTS**) nel membro flags della struttura [**ChooseFont**](/previous-versions/windows/desktop/legacy/ms646914(v=vs.85)) viene aggiunto per consentire la visualizzazione di tutti i tipi di carattere installati nell'elenco dei tipi di carattere, come **chooseFont** si è comportato prima Windows 7. Per informazioni dettagliate sulle differenze di comportamento Windows 7 per la funzione **ChooseFont,** vedere Finestra di dialogo comune [**Win32 ChooseFont()**](../win7appqual/choosefont-win32-common-dialog.md) nel Windows [7 Application Quality Cookbook](../win7appqual/windows-7-application-quality-cookbook.md). Fare riferimento alla **funzione ChooseFont** e alla **struttura CHOOSEFONT** per le differenze dell'esperienza utente finale in Windows 7.

Si noti che i set di caratteri sono una nozione legacy corrispondente ai set di caratteri pre-Unicode. Al momento non esiste alcun meccanismo per filtrare i tipi di carattere in base a script Unicode o intervalli di caratteri.

## <a name="font-controls-in-windows-scenic-ribbon"></a>Controlli carattere nella barra multifunzione Windows Panoramica

Windows 7 introduce la Windows Panoramic Ribbon, che include un set di controlli destinati alla selezione del tipo di carattere. Questi controlli dei tipi di carattere supportano il nuovo comportamento di Windows 7 caratteri nascosti. È possibile usare questi controlli per elencare solo i tipi di carattere visualizzati e consentire all'utente di selezionare il tipo di carattere.

> [!Note]  
> Il supporto per nascondere i tipi di carattere non è disponibile quando l'Windows Panoramic Ribbon è in esecuzione su qualsiasi piattaforma precedente a Windows 7.

 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**EnumFontFamiliesEx**](/windows/win32/api/wingdi/nf-wingdi-enumfontfamiliesexa)
</dt> <dt>

[**ChooseFont**](/previous-versions/windows/desktop/legacy/ms646914(v=vs.85))
</dt> <dt>

[**Struttura CHOOSEFONT**](/windows/win32/api/commdlg/ns-commdlg-choosefonta)
</dt> <dt>

[**Controlli carattere nella barra multifunzione Windows Panoramica**](../windowsribbon/windowsribbon-element-fontcontrol.md)
</dt> <dt>

[**Finestra di dialogo Comune ChooseFont() Win32**](../win7appqual/choosefont-win32-common-dialog.md)
</dt> </dl>

 

 
