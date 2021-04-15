---
description: È possibile installare assembly side-by-side come assembly condivisi o come assembly privati. Per ulteriori informazioni, vedere installazione di assembly side-by-side come assembly privati e installazione affiancata di assembly come assembly condivisi.
ms.assetid: 36f271ff-be0c-4162-8e1c-86088ebddbcc
title: Installazione di assembly affiancati
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3be68580c7f0e3890c2e53b148daec92fbad18ae
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104484637"
---
# <a name="installing-side-by-side-assemblies"></a>Installazione di assembly affiancati

È possibile installare assembly side-by-side come [assembly condivisi](/windows/desktop/Msi/shared-assemblies) o come [assembly privati](/windows/desktop/Msi/private-assemblies). Per ulteriori informazioni, vedere [installazione di assembly side-by-side come assembly privati](installing-side-by-side-assemblies-as-private-assemblies.md) e [installazione affiancata di assembly come assembly condivisi](installing-side-by-side-assemblies-as-shared-assemblies.md).

Tenere presente quanto segue:

-   Gli assembly installati nel Global Assembly Cache da un'installazione di che utilizza il [contesto di installazione](/windows/desktop/Msi/installation-context) per utente non sono protetti da protezione file di Windows.
-   Gli assembly installati nel Global Assembly Cache da un'installazione di tramite il [contesto di installazione](/windows/desktop/Msi/installation-context) per computer sono protetti da protezione file di Windows.

 

 
