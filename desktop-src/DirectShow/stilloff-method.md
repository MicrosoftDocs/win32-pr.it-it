---
description: Il metodo StillOff riprende la riproduzione, annullando la modalità ancora.
ms.assetid: 62091aad-8a78-4543-a844-a4227aed81df
title: Metodo StillOff
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d8986b62585768b83fc5737012a924e6cf33daf5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106314405"
---
# <a name="stilloff-method"></a>Metodo StillOff

> [!Note]  
> Questo componente è disponibile per l'uso nei sistemi operativi Microsoft Windows 2000, Windows XP e Windows Server 2003. È possibile che in versioni successive sia stata modificata o non sia più disponibile.

 

Il `StillOff` Metodo riprende la riproduzione, annullando la modalità ancora.

``` syntax
MSWebDVD.StillOff()
```

## <a name="return-value"></a>Valore restituito

Nessun valore restituito.

## <a name="remarks"></a>Commenti

Il [navigatore DVD](dvd-navigator-filter.md) passa alla modalità ancora quando rileva un frame ancora creato sul disco. Invia una notifica all'applicazione inviando un \_ DVD EC \_ ancora \_ in un evento. La modalità ancora è diversa da quella in cui lo strumento di spostamento DVD si trova in uno stato di sospensione a causa di un'operazione dell'utente. `StillOff`La chiamata riprende la riproduzione dalla modalità ancora, ma non riavvia il navigatore DVD quando si trova in uno stato di sospensione.

 

 



