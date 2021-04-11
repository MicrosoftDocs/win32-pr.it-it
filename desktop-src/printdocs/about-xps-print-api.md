---
description: XPS&\# 160; Stampa&\# 160; API fornisce un'interfaccia allo spooler di stampa che le applicazioni possono utilizzare per stampare processi che inviano documenti XPS a una stampante.
ms.assetid: d3bf7b1d-df21-4e7b-803b-45b65d46b2ca
title: Informazioni sull'API di stampa XPS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0b1467458a737a6faaddb5ed45c81623207ccdb2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104131603"
---
# <a name="about-the-xps-print-api"></a>Informazioni sull'API di stampa XPS

L' [API di stampa XPS](xps-printing.md) fornisce un'interfaccia allo spooler di stampa che le applicazioni possono utilizzare per stampare processi che inviano documenti XPS a una stampante.

Se la stampante di destinazione utilizza un driver della stampante XPSDrv, l'API di stampa XPS consente al driver della stampante XPSDrv di ricevere eventi di documento durante l'elaborazione di un processo di stampa da parte dello spooler di stampa. Per una descrizione degli eventi di documento inviati al driver della stampante XPSDrv, vedere [eventi del documento del driver XPS](/windows-hardware/drivers/print/xps-driver-document-events).

Se la stampante di destinazione utilizza un driver della stampante GDI, l' [API di stampa XPS](xps-printing.md) consente al sistema di gestire la necessaria conversione dei dati del processo di stampa dal formato XPS al formato Enhanced Metafile (EMF) utilizzato dal driver della stampante GDI. Per una descrizione degli eventi del documento del driver della stampante GDI, vedere [funzione DocumentEvent](documentevent.md).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Uso dell'API di stampa XPS](using-the-xps-print-api.md)
</dt> <dt>

[Informazioni di riferimento sulle API di stampa XPS](xpsprint-api.md)
</dt> </dl>

 

 
