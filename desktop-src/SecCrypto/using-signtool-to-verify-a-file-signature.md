---
description: Viene illustrato come usare SignTool per verificare la firma di un file.
ms.assetid: 9c40a397-19ea-4600-97ee-987dd10f4ef8
title: Uso di SignTool per verificare una firma file
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 137a4117b64ca5d62ee2ffe5fb80a7e0751d91f840ce1270482d9e114f4dd61b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118896694"
---
# <a name="using-signtool-to-verify-a-file-signature"></a>Uso di SignTool per verificare una firma file

Il comando seguente verifica la firma di un file denominato *MyControl.exe*:

**Verifica signTool** *MyControl.exe*

Se l'esempio precedente ha esito negativo, la firma potrebbe usare un certificato di firma del codice. [Il valore predefinito](signtool.md) di SignTool è il criterio Windows driver per la verifica.

Il comando seguente verifica la firma usando i criteri di verifica dell'autenticazione predefiniti:

**SignTool verify /pa** *MyControl.exe*

Il comando seguente verifica un file di sistema che può essere firmato in un catalogo:

**Verifica signTool /a** *SysFile.dll*

Il comando seguente verifica un file di sistema firmato in un catalogo denominato *MyCat.cat*:

**SignTool verify /c** *MyCat.cat* *MyFile.ini*

Per qualsiasi [verifica SignTool,](signtool.md) è possibile recuperare il firmatario del certificato. Il comando seguente verifica un file di sistema e visualizza il certificato del firmatario:

**Verifica signTool /v** *MyControl.exe*

[SignTool](signtool.md) restituisce il testo della riga di comando che indica il risultato del controllo della firma. SignTool restituisce inoltre un codice di uscita pari a zero per l'esecuzione corretta, uno per l'esecuzione non riuscita e due per l'esecuzione completata con avvisi.

Per altre informazioni su [SignTool,](signtool.md)vedere [SignTool](signtool.md).

 

 



