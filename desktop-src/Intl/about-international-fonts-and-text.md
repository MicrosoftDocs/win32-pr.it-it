---
description: Negli argomenti di questa sezione vengono trattate le funzionalità di base dei tipi di carattere internazionali.
ms.assetid: a47303b5-f49b-4d6c-b061-9d6475530e83
title: Gestione dei caratteri internazionali
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6d4c44661b234a95abb4d40f2204382b3d074bf1d7c0bb1c68a241345211695f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120083051"
---
# <a name="international-font-management"></a>Gestione dei caratteri internazionali

Negli argomenti di questa sezione vengono trattate le funzionalità di base dei tipi di carattere internazionali. Per istruzioni sull'uso della tecnologia dei tipi di carattere internazionale nelle applicazioni, vedere [Enumerazione](using-international-fonts-and-text.md) e selezione dei caratteri internazionali e Uso di [MS Shell Dlg e MS Shell Dlg 2.](using-ms-shell-dlg-and-ms-shell-dlg-2.md)

## <a name="font-management-infrastructure"></a>Infrastruttura di gestione dei caratteri

A partire da Windows 7, l'infrastruttura di gestione dei tipi di carattere supporta l'nascondere i tipi di carattere che non sono appropriati per gli elenchi di selezione dei tipi di carattere di un utente. Le impostazioni di sistema predefinite sceglieranno di nascondere automaticamente i tipi di carattere non progettati per le lingue di input (tastiere) abilitate nel sistema operativo. Inoltre, gli utenti possono scegliere di nascondere manualmente i tipi di carattere nel Pannello di controllo. Questa funzionalità significa che gli utenti non devono più dover affrontare lunghi elenchi di tipi di carattere non appropriati ed è particolarmente utile per gli utenti internazionali che lavorano in script non latini.

In Windows 7 non sono disponibili API per eseguire query direttamente su quali tipi di carattere sono nascosti o per impostare i tipi di carattere da nascondere. Tuttavia, questo non significa che non è possibile sfruttare questa funzionalità nell'applicazione. Se si usa l'API [**ChooseFont**](/previous-versions/windows/desktop/legacy/ms646914(v=vs.85)) Windows (finestra di dialogo Comune tipo di carattere) per abilitare la selezione dei tipi di carattere, si otterrà gratuitamente il nuovo comportamento. Il nuovo Windows panoramico (controlli carattere) introdotto in Windows 7 supporta anche questo comportamento e fornisce un altro motivo per "Ribbonize" le applicazioni. Per informazioni dettagliate sull'uso dei controlli carattere nella barra multifunzione e **scegliFont** per visualizzare i tipi di carattere mentre si filtrano i tipi di carattere nascosti, vedere Enumerazione e selezione dei tipi [di carattere internazionali](using-international-fonts-and-text.md).

Si noti che nascondere i tipi di carattere influisce solo sull'interfaccia utente di selezione dei tipi di carattere. Non influisce sulle API di disegno. Quando un tipo di carattere viene selezionato in un contesto di dispositivo, il disegno non ha alcun effetto a causa del tipo di carattere nascosto. La [**funzione EnumFontFamiliesEx**](/windows/win32/api/wingdi/nf-wingdi-enumfontfamiliesexa) continua a enumerare i tipi di carattere impostati su hidden.

## <a name="gdi-font-embedding-and-subsetting"></a>Incorporamento e subset dei tipi di carattere GDI

La tecnologia Tipi di carattere internazionali usa la libreria dei servizi di incorporamento dei tipi di carattere per consentire l'aggregazione dei tipi di carattere TrueType e OpenType in un documento o in un file. L'incorporamento di un tipo di carattere in un file garantisce che il tipo di carattere sia presente nel computer che riceve il file. Per altre informazioni, vedere [Informazioni di riferimento sull'incorporamento dei tipi di carattere.](../gdi/font-embedding-reference.md)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Enumerazione e selezione dei caratteri internazionali](using-international-fonts-and-text.md)
</dt> <dt>

[Uso di MS Shell Dlg e MS Shell Dlg 2](using-ms-shell-dlg-and-ms-shell-dlg-2.md)
</dt> <dt>

[Informazioni di riferimento per l'incorporamento dei tipi di carattere](../gdi/font-embedding-reference.md)
</dt> </dl>

 

 
