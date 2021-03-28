---
title: Informazioni sul driver di dispositivo
description: I driver e i moduli di dispositivo sono simili in quanto sono entrambi basati su file PE.
ms.assetid: 4f4ec15b-5592-4fe3-b754-fda25ab24159
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0735e791b8c6e1fc7434decc7ac71ccb5c1c469e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104044338"
---
# <a name="device-driver-information"></a>Informazioni sul driver di dispositivo

I driver e i moduli di dispositivo sono simili in quanto sono entrambi basati su file PE. Tuttavia, mentre ogni processo dispone di un proprio elenco privato di moduli caricati, i driver di dispositivo hanno moduli globali per il sistema. Di conseguenza, PSAPI dispone di funzioni specifiche per ottenere l'elenco dei driver di dispositivo e i relativi nomi.

È possibile recuperare l'indirizzo di caricamento per ogni driver di dispositivo chiamando la funzione [**EnumDeviceDrivers**](/windows/desktop/api/Psapi/nf-psapi-enumdevicedrivers) . Questa funzione riempie una matrice di valori **LPVOID** con gli indirizzi di caricamento di tutti i driver di dispositivo nel sistema.

La funzione [**GetDeviceDriverBaseName**](/windows/desktop/api/Psapi/nf-psapi-getdevicedriverbasenamea) accetta un indirizzo di caricamento del driver come input e compila un buffer con il nome di base del driver, ad esempio Win32k.sys. Una funzione correlata, [**GetDeviceDriverFileName**](/windows/desktop/api/Psapi/nf-psapi-getdevicedriverfilenamea), accetta gli stessi parametri e restituisce il percorso al driver di dispositivo (ad esempio, C: \\ Windows \\ system32 \\Win32k.sys).

 

 




