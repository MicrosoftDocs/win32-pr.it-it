---
description: La classe di dispositivo comm/DataModel/PortName è costituita dai nomi dei dispositivi a cui sono collegati i modem.
ms.assetid: 174519f6-3e73-4f05-9718-9e38680a0fb7
title: comm/DataModel/PortName
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e5f926dc87a093f49d41256b003e47c048caa5ac
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103883565"
---
# <a name="commdatamodemportname"></a>comm/DataModel/PortName

La classe di dispositivo comm/DataModel/PortName è costituita dai nomi dei dispositivi a cui sono collegati i modem. Quando il nome del dispositivo viene specificato in una chiamata alla funzione [**lineGetID**](/windows/desktop/api/Tapi/nf-tapi-linegetid) , la funzione compila la struttura [**VARSTRING**](/windows/desktop/api/Tapi/ns-tapi-varstring) con una stringa ANSI (not Unicode) con terminazione null che specifica il nome della porta a cui è collegato il modem specificato, ad esempio "COM1 \\ 0". Questa operazione è destinata principalmente ai fini dell'identificazione nell'interfaccia utente, ma può essere usata in alcune circostanze per aprire direttamente il dispositivo, ignorando il provider di servizi (se il provider di servizi non dispone già del dispositivo aperto). Se al dispositivo non è associata alcuna porta, \\ nella struttura **VARSTRING** viene restituita una stringa null ("0") (con una lunghezza di stringa pari a 1).

 

 



