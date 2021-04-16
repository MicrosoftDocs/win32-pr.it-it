---
description: In ogni versione principale di Windows sono stati aggiunti dei tipi di carattere per supportare lingue e script internazionali.
ms.assetid: 77b8c200-2682-4651-855a-602f768edc9b
title: Selezione e enumerazione dei tipi di carattere internazionali
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 63e5d0d07a0953f72f097f8578f5e32b3ee49093
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104350276"
---
# <a name="international-font-enumeration-and-selection"></a>Selezione e enumerazione dei tipi di carattere internazionali

In ogni versione principale di Windows sono stati aggiunti dei tipi di carattere per supportare lingue e script internazionali. Per i tipi di carattere aggiunti in ogni versione di Windows a partire da Windows 2000, nonché per gli script, le aree e i linguaggi supportati, fare riferimento al [supporto per script e tipi di carattere in Windows](https://msdn.microsoft.com/globalization/mt791278) .

## <a name="enumfontfamiliesex"></a>EnumFontFamiliesEx

Per enumerare i tipi di carattere internazionali nell'applicazione, è possibile usare la funzione [**EnumFontFamiliesEx**](/windows/win32/api/wingdi/nf-wingdi-enumfontfamiliesexa) . **EnumFontFamiliesEx** consente di enumerare i tipi di carattere in base al nome e al set di caratteri del carattere tipografico passando un puntatore a una struttura [**LOGFONT**](/windows/win32/api/wingdi/ns-wingdi-logfonta) che contiene le informazioni sul nome e sul set di caratteri. Per chiamare **EnumFontFamiliesEx**, è possibile specificare un nome di carattere tipografico o un set di caratteri oppure è possibile richiedere qualsiasi valore disponibile. L'impostazione del nome tipografico di **LOGFONT** su **null** enumera tutti i nomi dei caratteri tipografici. Impostando il campo CharSet **sul \_ set** di caratteri predefinito vengono enumerati tutti i set di caratteri.

Si noti che i set di caratteri sono una nozione legacy corrispondente a set di caratteri pre-Unicode. Al momento non è disponibile alcun meccanismo per enumerare i tipi di carattere che supportano gli script arbitrari o gli intervalli di caratteri in Unicode. La struttura [**NEWTEXTMETRICEX**](/windows/win32/api/wingdi/ns-wingdi-newtextmetricexa) passata da [**EnumFontFamExProc**](/previous-versions//dd162618(v=vs.85)) include la struttura [**FONTSIGNATURE**](/windows/win32/api/wingdi/ns-wingdi-fontsignature) , che include dichiarazioni più dettagliate fornite dallo sviluppatore di tipi di carattere per le tabelle codici e gli intervalli Unicode supportati dal tipo di carattere. Per determinare più precisamente gli intervalli di caratteri supportati da un determinato tipo di carattere, selezionare il tipo di carattere in un contesto di dispositivo e chiamare [**GetFontUnicodeRanges**](/windows/win32/api/wingdi/nf-wingdi-getfontunicoderanges). Si noti che questa API non supporta i piani supplementari Unicode.

## <a name="choosefont"></a>ChooseFont

È possibile usare la funzione [**ChooseFont**](/previous-versions/windows/desktop/legacy/ms646914(v=vs.85)) per visualizzare una finestra di dialogo comune che consente all'utente di selezionare i tipi di carattere internazionali in base al set di caratteri. È possibile specificare uno dei tre flag per determinare, in base al set di caratteri, i tipi di carattere visualizzati nella finestra di dialogo ChooseFont: **CF \_ SCRIPTSONLY**, **CF \_ SELECTSCRIPT** o **CF \_ NOSCRIPTSEL**.

Il flag **CF \_ SCRIPTSONLY** indica all'API di elencare i tipi di carattere per tutti i set di caratteri che non sono simboli o OEM.

Se si desidera visualizzare solo i tipi di carattere che coprono un set di caratteri specifico, è necessario specificare il flag **CF \_ SELECTSCRIPT**. Prima di chiamare [**ChooseFont**](/previous-versions/windows/desktop/legacy/ms646914(v=vs.85)), inizializzare il campo *LfCharSet* della struttura [**LOGFONT**](/windows/win32/api/wingdi/ns-wingdi-logfonta) . Se si è interessati a specificare solo il set di caratteri, impostare gli altri campi della struttura **LOGFONT** su **null**. Per fare in modo che **ChooseFont** osservi la struttura **LOGFONT** , è necessario specificare anche il flag **CF \_ INITTOLOGFONTSTRUCT** .

Infine, come per qualsiasi altro campo nella finestra di dialogo tipo di carattere, è possibile scegliere di visualizzare una casella di riepilogo script vuota. Questa funzionalità è utile se l'utente ha evidenziato più tipi di carattere diversi che si estendono su diversi set di caratteri. In questo caso, è necessario chiamare [**ChooseFont**](/previous-versions/windows/desktop/legacy/ms646914(v=vs.85)) con il flag **CF \_ NOSCRIPTSEL** .

A partire da Windows 7, [**ChooseFont**](/previous-versions/windows/desktop/legacy/ms646914(v=vs.85)) implementa il supporto per nascondere i tipi di carattere dagli elenchi di selezione dei tipi di carattere. **ChooseFont** elenca solo i tipi di carattere visualizzati ed esclude i tipi di carattere nascosti durante la visualizzazione dei tipi di carattere nella casella di riepilogo. Viene aggiunto il flag aggiuntivo (**CF \_ INACTIVEFONTS**) nel membro flag della struttura [**ChooseFont**](/previous-versions/windows/desktop/legacy/ms646914(v=vs.85)) per consentire la visualizzazione di tutti i tipi di carattere installati nell'elenco dei tipi di carattere, uguale a quello di **ChooseFont** prima di Windows 7. Per informazioni dettagliate sulle differenze di funzionamento in Windows 7 per la funzione **ChooseFont** , vedere la [**finestra di dialogo comune di ChooseFont () Win32**](../win7appqual/choosefont-win32-common-dialog.md) nel Cookbook per la [qualità delle applicazioni di Windows 7](../win7appqual/windows-7-application-quality-cookbook.md). Per informazioni sulle differenze di utilizzo dell'utente finale in Windows 7, fare riferimento alla funzione **ChooseFont** e alla struttura **ChooseFont** .

Si noti che i set di caratteri sono una nozione legacy corrispondente a set di caratteri pre-Unicode. Al momento non è disponibile alcun meccanismo per filtrare i tipi di carattere in base agli script Unicode o agli intervalli di caratteri.

## <a name="font-controls-in-windows-scenic-ribbon"></a>Controlli dei tipi di carattere nella barra multifunzione Windows Scenic

In Windows 7 è stata introdotta la barra multifunzione Windows Scenic che include un set di controlli destinati alla selezione dei tipi di carattere. Questi controlli dei tipi di carattere supportano il nuovo comportamento di nascondere i caratteri di Windows 7. È possibile utilizzare tali controlli per elencare solo i tipi di carattere visualizzati e consentire all'utente di selezionare il tipo di carattere.

> [!Note]  
> Il supporto per nascondere i tipi di carattere non è disponibile quando la barra multifunzione Windows Scenic è in esecuzione su qualsiasi piattaforma prima di Windows 7.

 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**EnumFontFamiliesEx**](/windows/win32/api/wingdi/nf-wingdi-enumfontfamiliesexa)
</dt> <dt>

[**ChooseFont**](/previous-versions/windows/desktop/legacy/ms646914(v=vs.85))
</dt> <dt>

[**Struttura CHOOSEFONT**](/windows/win32/api/commdlg/ns-commdlg-choosefonta)
</dt> <dt>

[**Controlli dei tipi di carattere nella barra multifunzione Windows Scenic**](../windowsribbon/windowsribbon-element-fontcontrol.md)
</dt> <dt>

[**ChooseFont () finestra di dialogo comune Win32**](../win7appqual/choosefont-win32-common-dialog.md)
</dt> </dl>

 

 
