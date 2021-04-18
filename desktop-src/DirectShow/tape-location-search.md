---
description: Ricerca posizione nastro
ms.assetid: 17fb4eba-4b2c-41c2-94e2-e58586f92e53
title: Ricerca posizione nastro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 33d1fb719f3b43374e5aa86f34c60e5b8f14d536
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106316297"
---
# <a name="tape-location-search"></a>Ricerca posizione nastro

Sebbene i dispositivi DV supportino un comando per la ricerca in base al codice temporale o al numero di traccia assoluto (ATN), il driver MSDV non dispone di un modo standard e indipendente dal dispositivo per accedere a queste funzioni. L'unica opzione consiste nell'inviare al driver un comando AV/C non elaborato, come descritto nell'argomento relativo all' [emissione di comandi AV/c non elaborati](issuing-raw-av-c-commands.md).

Il driver UVC supporta una proprietà impostata per le ricerche nel percorso del nastro. Per inviare un comando di ricerca, utilizzare l'interfaccia **IKsControl** e impostare la \_ proprietà del trasporto PROPSETID ext \_ . L'uso di un set di proprietà è più sicuro dell'invio di comandi AV/C non elaborati al dispositivo, perché i comandi AV/C ignorano il filtro e passano direttamente al driver di dispositivo.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Controllo di una videocamera DV](controlling-a-dv-camcorder.md)
</dt> <dt>

[Set di proprietà di trasporto dispositivo esterno](external-device-transport-property-set.md)
</dt> </dl>

 

 



