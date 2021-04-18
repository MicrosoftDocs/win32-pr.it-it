---
description: Viene illustrato come utilizzare SignTool per verificare una firma del file.
ms.assetid: 9c40a397-19ea-4600-97ee-987dd10f4ef8
title: Uso di SignTool per verificare una firma del file
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f8161d4c890400f3aa33b415e7ac16a5306aa094
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106308629"
---
# <a name="using-signtool-to-verify-a-file-signature"></a>Uso di SignTool per verificare una firma del file

Il comando seguente verifica la firma di un file denominato *MyControl.exe*:

**Verifica** *MyControl.exe* di SignTool

Se l'esempio precedente ha esito negativo, è possibile che la firma abbia utilizzato un certificato di firma codice. Per impostazione predefinita, [SignTool](signtool.md) è il criterio driver di Windows per la verifica.

Il comando seguente verifica la firma, usando i criteri di verifica dell'autenticazione predefiniti:

**SignTool Verify/pa** *MyControl.exe*

Il comando seguente verifica un file di sistema che può essere firmato in un catalogo:

**Verifica di SignTool/a** *SysFile.dll*

Il comando seguente verifica un file di sistema firmato in un catalogo denominato *MyCat.cat*:

**Verifica di SignTool/c** *MyCat.catMyFile.ini*

Per qualsiasi verifica di [SignTool](signtool.md) , è possibile recuperare il firmatario del certificato. Il comando seguente verifica un file di sistema e visualizza il certificato del firmatario:

**Verifica di SignTool** *MyControl.exe* /v

[SignTool](signtool.md) restituisce il testo della riga di comando che indica il risultato del controllo della firma. Inoltre, SignTool restituisce un codice di uscita pari a zero per l'esecuzione completata, uno per l'esecuzione non riuscita e due per l'esecuzione completata con avvisi.

Per ulteriori informazioni su [SignTool](signtool.md), vedere [SignTool](signtool.md).

 

 



