---
description: In questo argomento viene illustrato come stampare da un programma di Windows nativo usando GDI&\# 160; Stampa&\# 160; Api.
ms.assetid: C212DD92-2B90-45BC-8746-29C193FBDF69
title: "Procedura: Stampare usando l'API di stampa GDI"
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e19832ef93a80cc537d16136ac751cb20fd8664d7d1d31d295568de68d6dd846
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120091931"
---
# <a name="how-to-print-using-the-gdi-print-api"></a>Procedura: Stampare usando l'API di stampa GDI

In questo argomento viene illustrato come stampare da un programma Windows utilizzando [l'API di stampa GDI.](gdi-printing.md)

## <a name="overview"></a>Panoramica

La stampa è in genere parte integrante di un programma Windows nativo, quindi non è una funzionalità che è possibile aggiungere facilmente dopo aver scritto il programma. Quando si progetta un programma per Windows 7, è consigliabile usare l'API di stampa [XPS](xps-printing.md) per fornire la funzionalità di stampa perché offre la maggiore compatibilità per il futuro. I programmi che devono essere eseguiti Windows Vista e versioni precedenti di Windows molto probabilmente useranno l'API di stampa [GDI](gdi-printing.md) per fornire funzionalità di stampa. L'API di stampa GDI è supportata anche in Windows 7, ma è più limitata rispetto all'API di stampa XPS.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Uso della stampa](using-printing.md)
</dt> <dt>

[Come stampare da un'Windows applicazione](how-to--print-from-a-windows-application.md)
</dt> </dl>

 

 



