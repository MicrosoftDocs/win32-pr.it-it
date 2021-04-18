---
description: Se \_ viene specificato il flag SP Copy più \_ recente durante un'operazione di copia file, le funzioni di installazione verificano la presenza di una copia esistente del file nella directory di destinazione.
ms.assetid: fd493b5d-7bab-4450-a749-745c536902dc
title: Confronti tra versioni di file
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d9601dcef07afca81a3ffc64148b0c4f2492f935
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106316084"
---
# <a name="file-version-comparisons"></a>Confronti tra versioni di file

Se \_ viene specificato il flag SP Copy più \_ recente durante un'operazione di copia file, le funzioni di installazione verificano la presenza di una copia esistente del file nella directory di destinazione. Se viene trovata una copia esistente, le funzioni confrontano le versioni del file di destinazione e di origine per determinare quale è più recente.

Le informazioni sulla versione del file utilizzate durante i controlli della versione sono specificate nei membri **dwFileVersionMS** e **dwFileVersionLS** di una struttura [**vs \_ informazione FixedFileInfo**](/windows/win32/api/verrsrc/ns-verrsrc-vs_fixedfileinfo) , utilizzata dalle funzioni di versione. Se per uno dei file non sono state specificate risorse di versione o se hanno le stesse informazioni sulla versione, il file di origine viene considerato come il file più recente.

 

 
