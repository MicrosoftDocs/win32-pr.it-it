---
description: La classe di dispositivi comm è costituita da porte di comunicazione. Per accedere a questi dispositivi, è possibile usare le funzioni file e comunicazioni.
ms.assetid: c1cf4998-b752-4cfd-9dd7-c9872b62c44b
title: comunicazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 40136654d7e308f30e4e27467cf5e21385340841
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103752999"
---
# <a name="comm"></a>comunicazione

La classe di dispositivi comm è costituita da porte di comunicazione. Per accedere a questi dispositivi, è possibile usare le funzioni [file](/windows/desktop/FileIO/file-management-functions) e [comunicazioni](/windows/desktop/DevIO/communications-functions).

La funzione [**lineGetID**](/windows/desktop/api/Tapi/nf-tapi-linegetid) compila una struttura [**VARSTRING**](/windows/desktop/api/Tapi/ns-tapi-varstring) , impostando il membro **dwStringFormat** sul \_ valore ASCII STRINGFORMAT e aggiungendo una stringa con terminazione null che specifica il nome del dispositivo di comunicazione, ad esempio il nome del modem.

 

 
