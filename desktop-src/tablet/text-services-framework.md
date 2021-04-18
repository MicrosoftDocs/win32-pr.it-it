---
description: Panoramica del Framework di servizi di testo per il Tablet PC.
ms.assetid: f77fe77a-8625-47c5-bfc7-b473c8e8a8c6
title: Framework servizi di testo (Tablet PC)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c25eb3e635ae7394502ed203cb9ea31e115dc09e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106318686"
---
# <a name="text-services-framework-tablet-pc"></a>Framework servizi di testo (Tablet PC)

Quando il [Framework dei servizi di testo (TSF)](../tsf/text-services-framework.md) viene abilitato in un controllo con un oggetto [PenInputPanel](/previous-versions/aa514041(v=msdn.10)) collegato, l'oggetto PenInputPanel può inserire direttamente il testo. Se il controllo non supporta il Framework di servizi di testo (TSF), l'oggetto PenInputPanel deve ricorrere all'uso della [funzione SendInput](/windows/win32/api/winuser/nf-winuser-sendinput) per inserire il testo.

La possibilità di inserire testo direttamente diventa molto importante per i caratteri asiatici orientali, in cui l'uso della [funzione SendInput](/windows/win32/api/winuser/nf-winuser-sendinput) può produrre caratteri non corretti.

TSF fornisce un'interfaccia per la correzione degli errori di riconoscimento che consentono all'utente finale di correggere, riscrivere o persino dettare il testo appropriato.

TSF è abilitato chiamando il metodo [EnableTsf](/previous-versions/ms569656(v=vs.100)) con il parametro *Enable* impostato su **true**.

\[C\#\]


```C++
PenInputPanel thePenInputPanel = new PenInputPanel(theControl);
//...
thePenInputPanel.EnableTsf(true);
```



Un oggetto [PenInputPanel](/previous-versions/aa514041(v=msdn.10)) associato a un controllo [InkEdit](/previous-versions/ms552265(v=vs.100)) fornisce un'esperienza utente affidabile perché il InkEdit supporta TSF. Tuttavia, assicurarsi di impostare la proprietà [InkMode](/previous-versions/ms835850(v=msdn.10)) su [Microsoft. Ink. InkMode. Ink](/previous-versions/ms827399(v=msdn.10)) sul controllo InkEdit come indicato nell'argomento [procedure consigliate](best-practices.md) .

L'esempio [PenInputPanel](peninputpanel-sample.md) fornisce un esempio di abilitazione di TSF.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Text Services Framework](../tsf/text-services-framework.md)
</dt> </dl>

 

 
