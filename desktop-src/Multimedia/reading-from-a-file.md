---
title: Lettura da un file
description: Lettura da un file
ms.assetid: 7c728304-7d05-4e28-a9bd-83b5b1af39be
keywords:
- Funzione AVIFileInfo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ab95186b1ec8913623b0ab02e0d2bc5556302d4dcd03f7737ac12c5872b9f2fb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118371687"
---
# <a name="reading-from-a-file"></a>Lettura da un file

È possibile recuperare informazioni su un file aperto usando la [**funzione AVIFileInfo.**](/windows/desktop/api/Vfw/nf-vfw-avifileinfo) Questa funzione riempie la struttura [**AVIFILEINFO**](/windows/desktop/api/Vfw/ns-vfw-avifileinfoa) con informazioni quali la velocità massima dei dati, il numero di flussi nel file, se il file usa un indice e se il file è protetto da copyright.

Per recuperare informazioni supplementari in un file AVI, usare la [**funzione AVIFileReadData.**](/windows/desktop/api/Vfw/nf-vfw-avifilereaddata) Le informazioni supplementari sono applicabili all'intero file e non sono incluse nelle intestazioni di file normali. Ad esempio, il nome della società o della persona che possiede il copyright di un file potrebbe essere un'informazione supplementare. Le informazioni supplementari non sono conformi a un formato specifico. può essere specifico del file. **AVIFileReadData** restituisce le informazioni supplementari in un buffer fornito dall'applicazione.

 

 




