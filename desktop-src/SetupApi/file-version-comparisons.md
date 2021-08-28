---
description: Se durante un'operazione di copia di file viene specificato il flag SP COPY NEWER, le funzioni di installazione verificano la presenza di una copia esistente del \_ file nella directory di \_ destinazione.
ms.assetid: fd493b5d-7bab-4450-a749-745c536902dc
title: Confronti tra le versioni dei file
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a017549899aa43340f744b1176e7d14ce17d44d60c52b18cfbed9eae3474e99a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119683181"
---
# <a name="file-version-comparisons"></a>Confronti tra le versioni dei file

Se durante un'operazione di copia di file viene specificato il flag SP COPY NEWER, le funzioni di installazione verificano la presenza di una copia esistente del \_ file nella directory di \_ destinazione. Se viene trovata una copia esistente, le funzioni confrontano le versioni del file di origine e di destinazione per determinare quale è più recente.

Le informazioni sulla versione del file usate durante i controlli della versione sono specificate nei membri **dwFileVersionMS** e **dwFileVersionLS** di una struttura [**\_ FIXEDFILEINFO**](/windows/win32/api/verrsrc/ns-verrsrc-vs_fixedfileinfo) di VISUAL Studio, usata dalle funzioni di versione. Se per uno dei file non sono specificate risorse di versione o se hanno le stesse informazioni sulla versione, il file di origine viene considerato come il file più recente.

 

 
