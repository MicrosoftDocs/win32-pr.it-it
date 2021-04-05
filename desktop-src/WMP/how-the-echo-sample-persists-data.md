---
title: Modo in cui l'esempio Echo rende permanente i dati
description: Modo in cui l'esempio Echo rende permanente i dati
ms.assetid: be75760f-c378-45d1-99de-43ef0ec4b8f0
keywords:
- Plug-in di Windows Media Player, pagine delle proprietà di esempio Echo
- plug-in, pagine delle proprietà di esempio Echo
- plug-in di elaborazione dei segnali digitali, pagine delle proprietà di esempio Echo
- Plug-in DSP, pagine delle proprietà di esempio Echo
- Esempio di plug-in Echo DSP, pagine delle proprietà
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: df781754fd52639272850158187cb1258c081583
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103711560"
---
# <a name="how-the-echo-sample-persists-data"></a>Modo in cui l'esempio Echo rende permanente i dati

Quando Windows Media Player Abilita un plug-in DSP, può creare ed eliminare molte istanze dell'oggetto plug-in nel corso di una sessione. Il plug-in deve essere in grado di salvare in modo permanente i valori delle proprietà tra le istanze. Il codice di esempio generato dalla procedura guidata per il plug-in di Windows Media Player archivia questi valori nel registro di sistema e li recupera quando viene richiamata la pagina delle proprietà o quando viene creata una nuova istanza del plug-in.

Il codice di esempio predefinito in Echo. h include due costanti che archiviano il percorso del registro di sistema predefinito e la stringa del nome del fattore di scala. È necessario tenere la variabile che specifica il percorso, ma eliminare la riga che specifica il nome del registro di sistema del fattore di scala. Aggiungere quindi il codice seguente per definire le costanti per i nomi delle proprietà di tempo di ritardo e di combinazione Wet nel registro di sistema. La sezione operazione completata dovrebbe essere simile alla seguente:


```C++
// registry location for preferences
const TCHAR kszPrefsRegKey[] = _T("Software\\Echo\\DSP Plugin");
const TCHAR kszPrefsDelayTime[] = _T("DelayTime");
const TCHAR kszPrefsWetmix[] = _T("Wetmix");

```



Queste costanti vengono utilizzate quando si modificano i metodi della pagina delle proprietà.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Modifica della pagina delle proprietà di esempio Echo**](modifying-the-echo-sample-property-page.md)
</dt> </dl>

 

 




