---
description: Negli argomenti di questa sezione vengono illustrate le funzionalità di base dei tipi di carattere internazionali.
ms.assetid: a47303b5-f49b-4d6c-b061-9d6475530e83
title: Gestione dei tipi di carattere internazionali
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 96ade599577f97c696d3205e32bfaaca106ddaae
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106314310"
---
# <a name="international-font-management"></a>Gestione dei tipi di carattere internazionali

Negli argomenti di questa sezione vengono illustrate le funzionalità di base dei tipi di carattere internazionali. Per istruzioni sull'uso della tecnologia internazionale per i tipi di carattere nelle applicazioni, vedere [enumerazione e selezione dei tipi di carattere internazionali](using-international-fonts-and-text.md) e [utilizzo di MS Shell Dlg e MS Shell Dlg 2](using-ms-shell-dlg-and-ms-shell-dlg-2.md).

## <a name="font-management-infrastructure"></a>Infrastruttura di gestione dei tipi di carattere

A partire da Windows 7, l'infrastruttura di gestione dei tipi di carattere supporta il nascondimento di tipi di carattere non appropriati per gli elenchi di selezione dei tipi di carattere di un utente. Le impostazioni di sistema predefinite scelgono di nascondere automaticamente i tipi di carattere non progettati per le lingue di input (tastiere) abilitati nel sistema operativo. Inoltre, gli utenti possono scegliere di nascondere manualmente i tipi di carattere nel pannello di controllo dei tipi di carattere. Questa funzionalità significa che gli utenti non devono più affrontare lunghi elenchi di tipi di carattere non appropriati ed è particolarmente utile per gli utenti internazionali che lavorano in script non latini.

In Windows 7 non sono disponibili API per l'esecuzione diretta di query sui tipi di carattere nascosti o per l'impostazione di caratteri nascosti. Tuttavia, ciò non significa che non è possibile sfruttare questa funzionalità nell'applicazione. Se si usa l'API [**ChooseFont**](/previous-versions/windows/desktop/legacy/ms646914(v=vs.85)) di Windows (finestra di dialogo comune del tipo di carattere) per abilitare la selezione dei tipi di carattere oggi, si otterrà il nuovo comportamento gratuitamente. La nuova barra multifunzione Windows Scenic (controlli dei tipi di carattere) introdotta in Windows 7 supporta inoltre questo comportamento e fornisce un altro motivo per "Ribbonize" delle applicazioni. Per informazioni dettagliate sull'uso dei controlli dei tipi di carattere nella barra multifunzione e **ChooseFont** per visualizzare i tipi di carattere, è necessario fare riferimento all' [enumerazione e alla selezione](using-international-fonts-and-text.md)dei tipi di carattere internazionali.

Si noti che nascondere i caratteri influisca solo sull'interfaccia utente di selezione dei tipi di carattere Non influisca sulle API di disegno. Quando si seleziona un tipo di carattere in un contesto di dispositivo, non si verifica alcun effetto sul disegno a causa del tipo di carattere nascosto. La funzione [**EnumFontFamiliesEx**](/windows/win32/api/wingdi/nf-wingdi-enumfontfamiliesexa) continua a enumerare i tipi di carattere impostati su Hidden.

## <a name="gdi-font-embedding-and-subsetting"></a>Incorporamento e subimpostazione del tipo di carattere GDI

La tecnologia dei tipi di carattere internazionali Usa la libreria di servizi di incorporamento dei tipi di carattere per consentire l'aggregazione di tipi di carattere TrueType e OpenType in un documento o un file. Incorporando un tipo di carattere in un file si garantisce che il tipo di carattere sarà presente nel computer che riceve il file. Per altre informazioni, vedere [riferimento all'incorporamento dei tipi di carattere](../gdi/font-embedding-reference.md).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Selezione e enumerazione dei tipi di carattere internazionali](using-international-fonts-and-text.md)
</dt> <dt>

[Utilizzo di MS Shell Dlg e MS Shell Dlg 2](using-ms-shell-dlg-and-ms-shell-dlg-2.md)
</dt> <dt>

[Riferimento all'incorporamento dei tipi di carattere](../gdi/font-embedding-reference.md)
</dt> </dl>

 

 
