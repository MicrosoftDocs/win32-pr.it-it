---
description: ICEM13 verifica che il modulo di merge non contenga i criteri dell'editore e gli assembly di configurazione.
ms.assetid: 1281ee21-a154-4275-a9e6-6e92fff548ed
title: ICEM13
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 678b89e14cb699bb6207be5c2e14473de2a743494b47ff5ae5e0ccda2a9cc9cc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119894281"
---
# <a name="icem13"></a>ICEM13

ICEM13 verifica che il modulo di merge non contenga i criteri dell'editore e gli assembly di configurazione. Publisher gli assembly dei criteri e di configurazione non devono essere inclusi nei moduli unione destinati alla ridistribuzione, perché ciò può influire sulle altre applicazioni nel computer di un utente.

Questo icem è disponibile nel file Mergemod.cub disponibile in Windows Installer 2.0 SDK e versioni successive. Per informazioni dettagliate, vedere [Windows SDK Components for Windows Installer Developers](platform-sdk-components-for-windows-installer-developers.md).

## <a name="result"></a>Risultato

ICEM13 invia un messaggio di avviso se trova un componente specificato nel campo Componente della tabella [MsiAssembly](msiassembly-table.md) del modulo di merge che è un criterio dell'editore o un assembly di configurazione.

## <a name="example"></a>Esempio

ICEM13 invia il messaggio di avviso seguente se trova una riga nella tabella [MsiAssembly](msiassembly-table.md) con un componente ' 1 ' specificato nel campo Componente che è un criterio dell'editore o un assembly di configurazione incluso nel modulo \[ \] unione.

``` syntax
This entry Component_=`[1]` in MsiAssembly Table is a Policy/Configuration Assembly. A Publisher Policy/Configuration assembly should not be redistributed with a merge module. Policy/Configuration may impact other applications and should only be installed with products.
```

È possibile installare i criteri dell'editore e gli assembly di configurazione usando il programma di installazione di Windows. Non è consigliabile ridistribuire questi assembly nei moduli unione.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Informazioni di riferimento sul modulo di unione ICE](merge-module-ice-reference.md)
</dt> </dl>

 

 



