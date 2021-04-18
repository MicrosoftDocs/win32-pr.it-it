---
description: ICE74 verifica che la proprietà FASTOEM non sia stata creata nella tabella delle proprietà.
ms.assetid: 2af132f0-0ffa-405f-9d05-7cb5d5f826b8
title: ICE74
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6fe2762710e061f2c88f55893294a40fbac8700f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106308323"
---
# <a name="ice74"></a>ICE74

ICE74 verifica che la proprietà [**FASTOEM**](fastoem.md) non sia stata creata nella [tabella delle proprietà](property-table.md).

La proprietà [**FASTOEM**](fastoem.md) consente agli OEM di ridurre il tempo necessario per installare le applicazioni Windows Installer per la prima volta. Non può essere utilizzata dopo la prima installazione. La proprietà **FASTOEM** non deve essere creata nella tabella delle proprietà perché questa operazione interferisce con le installazioni successive per la manutenzione, la rimozione o il ripristino dell'applicazione.

ICE74 verifica inoltre che la proprietà [**UpgradeCode**](upgradecode.md) sia stata creata nella tabella delle [Proprietà](property-table.md)e che il relativo valore non sia un GUID null, {00000000-0000-0000-0000-000000000000} .

## <a name="result"></a>Risultato

ICE74 può inserire i seguenti errori.



| Errore ICE74                                                                       | Descrizione                                                                                             |
|-----------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------|
| Impossibile creare la proprietà [**FASTOEM**](fastoem.md) nella tabella delle proprietà. | La proprietà [**FASTOEM**](fastoem.md) è stata impostata nella tabella delle proprietà.                             |
| ' \[ 2 \] ' non è un [**UpgradeCode**](upgradecode.md)valido.                        | È stato immesso un GUID null per la proprietà [**UpgradeCode**](upgradecode.md) nella tabella delle proprietà. |



 

ICE74 può inviare il seguente avviso.



| Avviso di ICE74                                                                                                                                                                                             | Descrizione                                                                            |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| La proprietà [**UpgradeCode**](upgradecode.md) non è stata creata nella tabella delle proprietà. Si consiglia vivamente agli autori dei pacchetti di installazione di specificare un **UpgradeCode** per la propria applicazione. | La proprietà [**UpgradeCode**](upgradecode.md) non è stata creata nella tabella delle proprietà. |



 

## <a name="example"></a>Esempio

ICE74 segnala l'errore seguente se la proprietà [**FASTOEM**](fastoem.md) è impostata: FASTOEM

``` syntax
 property cannot be authored in the Property table.
```

[Tabella delle proprietà](property-table.md) (parziale)



| Proprietà                   | Valore |
|----------------------------|-------|
| [**FASTOEM**](fastoem.md) | 1     |



 

Per correggere l'errore, rimuovere la proprietà [**FASTOEM**](fastoem.md) dalla tabella delle proprietà.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Proprietà FASTOEM**](fastoem.md)
</dt> <dt>

[Tabella delle proprietà](property-table.md)
</dt> <dt>

[Riferimento ghiaccio](ice-reference.md)
</dt> </dl>

 

 



