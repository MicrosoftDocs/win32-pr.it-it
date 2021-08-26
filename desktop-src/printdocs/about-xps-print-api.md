---
description: XpS&\# 160; Stampa&\# 160; L'API fornisce un'interfaccia per lo spooler di stampa che le applicazioni possono usare per stampare processi che inviano documenti XPS a una stampante.
ms.assetid: d3bf7b1d-df21-4e7b-803b-45b65d46b2ca
title: Informazioni sull'API di stampa XPS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8e43c0bde59424c220e3d3ea9eab4b4780ace425cab28882013853a72d422815
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119950861"
---
# <a name="about-the-xps-print-api"></a>Informazioni sull'API di stampa XPS

[L'API di stampa XPS](xps-printing.md) fornisce un'interfaccia per lo spooler di stampa che le applicazioni possono usare per stampare processi che inviano documenti XPS a una stampante.

Se la stampante di destinazione usa un driver della stampante XPSDrv, l'API di stampa XPS consente al driver della stampante XPSDrv di ricevere eventi di documento durante l'elaborazione di un processo di stampa da parte dello spooler di stampa. Per una descrizione degli eventi del documento inviati al driver della stampante XPSDrv, vedere [XpS Driver Document Events](/windows-hardware/drivers/print/xps-driver-document-events).

Se la stampante di destinazione usa un driver della stampante GDI, l'API di stampa [XPS](xps-printing.md) consente al sistema di gestire la conversione necessaria dei dati del processo di stampa dal formato XPS al formato Enhanced Metafile (EMF) utilizzato dal driver della stampante GDI. Per una descrizione degli eventi del documento del driver della stampante GDI, vedere [Funzione DocumentEvent](documentevent.md).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Uso dell'API di stampa XPS](using-the-xps-print-api.md)
</dt> <dt>

[Informazioni di riferimento sulle API di stampa XPS](xpsprint-api.md)
</dt> </dl>

 

 
