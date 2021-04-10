---
description: ICEM13 verifica che il modulo merge non contenga gli assembly di configurazione e i criteri del server di pubblicazione.
ms.assetid: 1281ee21-a154-4275-a9e6-6e92fff548ed
title: ICEM13
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3286906cf162f24dce7105835544c3a387993ac6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103881049"
---
# <a name="icem13"></a>ICEM13

ICEM13 verifica che il modulo merge non contenga gli assembly di configurazione e i criteri del server di pubblicazione. I criteri e gli assembly di configurazione del server di pubblicazione non devono essere inclusi nei moduli unione destinati alla ridistribuzione perché possono influire su altre applicazioni nel computer di un utente.

Questo ICEM è disponibile nel file Mergemod. cub fornito in Windows Installer SDK 2,0 e versioni successive. Per informazioni dettagliate, vedere [Windows SDK Components for Windows Installer Developers](platform-sdk-components-for-windows-installer-developers.md).

## <a name="result"></a>Risultato

ICEM13 Invia un messaggio di avviso se trova un componente specificato nel campo componente della [tabella MsiAssembly](msiassembly-table.md) del modulo merge, ovvero un criterio editore o un assembly di configurazione.

## <a name="example"></a>Esempio

ICEM13 invia il seguente messaggio di avviso se trova una riga nella [tabella MsiAssembly](msiassembly-table.md) con un componente " \[ 1 \] " specificato nel campo componente, ovvero un criterio editore o un assembly di configurazione che è stato incluso nel modulo unione.

``` syntax
This entry Component_=`[1]` in MsiAssembly Table is a Policy/Configuration Assembly. A Publisher Policy/Configuration assembly should not be redistributed with a merge module. Policy/Configuration may impact other applications and should only be installed with products.
```

È possibile installare i criteri editore e gli assembly di configurazione utilizzando la Windows Installer, non è consigliabile ridistribuire questi assembly nei moduli unione.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Riferimento ghiaccio del modulo merge](merge-module-ice-reference.md)
</dt> </dl>

 

 



