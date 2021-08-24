---
description: Modifica successiva dell'area DVD
ms.assetid: 08c0b48a-2851-40c8-addc-21baeb83df1b
title: Modifica successiva dell'area DVD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b6da91ff9fefb17480bbc502deb2fea80683e5861d32cfa4d4fa1a5cb22c2847
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119633291"
---
# <a name="subsequent-dvd-region-change"></a>Modifica successiva dell'area DVD

In Windows 2000 e versioni successive, lo strumento di spostamento DVD richiama una pagina delle proprietà nel dispositivo unità DVD-ROM in Gestione dispositivi. Questa pagina delle proprietà viene visualizzata anche dall'applicazione DVDPlay.exe quando è necessario modificare un'area. L'interfaccia utente di questa pagina delle proprietà è molto simile a quella DVDRgn.exe e viene regionalizzata nel sistema operativo.

Per le unità RPC1, i componenti Windows sistema operativo gestiscono le modifiche all'area. Le unità RPC2 mantengono l'impostazione dell'area nel proprio hardware. Quando il numero di modifiche consentite viene esaurito in un'unità RPC2, l'unità non riuscirà la chiamata per modificare l'area e il componente di modifica dell'area nel sistema operativo indicherà che all'utente.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Supporto della modifica dell'area DVD in Windows](dvd-region-change-support-in-windows.md)
</dt> </dl>

 

 



