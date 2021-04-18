---
description: La classe del dispositivo TAPI/terminal è costituita dai dispositivi telefonici associati a ogni terminale su una linea o dal terminale in ogni riga associata a un dispositivo telefonico. Per accedere a questi dispositivi, è possibile usare il dispositivo linea TAPI o le funzioni del dispositivo telefonico.
ms.assetid: 466ed2cd-f737-4df4-8633-4fb5c95b4b6c
title: TAPI/terminale
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dce64da984f766e8ca3c0c47f1b60db6e9d7d8ed
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106315263"
---
# <a name="tapiterminal"></a>TAPI/terminale

La classe del dispositivo TAPI/terminal è costituita dai dispositivi telefonici associati a ogni terminale su una linea o dal terminale in ogni riga associata a un dispositivo telefonico. Per accedere a questi dispositivi, è possibile usare il [dispositivo linea](line-device-functions.md) TAPI o le [funzioni del dispositivo telefonico](phone-device-functions.md).

La funzione [**lineGetID**](/windows/desktop/api/Tapi/nf-tapi-linegetid) compila una struttura [**VARSTRING**](/windows/desktop/api/Tapi/ns-tapi-varstring) , impostando il membro **dwStringFormat** sul \_ valore binario STRINGFORMAT e aggiungendo il membro aggiuntivo seguente:

``` syntax
DWORD adwDeviceId[];  // array of phone device identifiers
```

Il membro **adwDeviceId** è una matrice di identificatori di dispositivi telefonici. È presente un elemento di matrice per ogni terminale specificato dal membro **dwNumTerminals** nella struttura [**LINEDEVCAPS**](/windows/desktop/api/Tapi/ns-tapi-linedevcaps) per il dispositivo di linea specificato. Ogni elemento specifica l'identificatore del dispositivo telefonico associato al terminale corrispondente sulla riga. Se non è presente alcun dispositivo telefonico associato a un terminale, l'elemento viene impostato su-1 (0xFFFFFFFF).

La funzione [**phoneGetID**](/windows/desktop/api/Tapi/nf-tapi-phonegetid) compila una struttura [**VARSTRING**](/windows/desktop/api/Tapi/ns-tapi-varstring) , impostando il membro **dwStringFormat** sul \_ valore binario STRINGFORMAT e aggiungendo il membro aggiuntivo seguente:

``` syntax
DWORD adwTerminalID[];  // array of terminal identifiers
```

Il membro **adwTerminalID** è una matrice di identificatori di terminale. È presente un elemento di matrice per ogni identificatore di dispositivo linea specificato dalla funzione [**lineInitialize**](/windows/desktop/api/Tapi/nf-tapi-lineinitialize) o [**lineInitializeEx**](/windows/desktop/api/Tapi/nf-tapi-lineinitializeexa) . Ogni elemento della matrice contiene l'identificatore del terminale associato al dispositivo telefonico per il dispositivo di linea specificato. Se non è presente alcun dispositivo telefonico, l'elemento viene impostato su-1 (0xFFFFFFFF). Gli identificatori di terminale hanno un valore compreso tra zero e uno inferiore al numero specificato dal membro **dwNumTerminals** nella struttura [**LINEDEVCAPS**](/windows/desktop/api/Tapi/ns-tapi-linedevcaps) .

 

 



