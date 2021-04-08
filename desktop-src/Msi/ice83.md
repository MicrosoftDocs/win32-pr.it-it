---
description: ICE83 convalida la tabella MsiAssembly.
ms.assetid: dd290c73-6528-482d-8276-ac56d0fec181
title: ICE83
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d5ac38b4455875314c85fa08c1cfdc329e0cb470
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104049903"
---
# <a name="ice83"></a>ICE83

ICE83 convalida la [tabella MsiAssembly](msiassembly-table.md). Questa azione personalizzata ICE Invia un errore se il percorso della chiave per un componente contenente un assembly Win32 è impostato sul file manifesto. In modo esplicito, l'errore viene inserito se il valore immesso nel campo del percorso della [tabella dei componenti](component-table.md) è uguale al valore immesso nel \_ campo del manifesto del file della tabella MsiAssembly. Questa azione personalizzata ICE Invia un errore se esiste almeno un record nella tabella MsiAssembly e la [tabella InstallExecuteSequence](installexecutesequence-table.md) non contiene sia l'azione [MsiPublishAssemblies](msipublishassemblies-action.md) che l' [azione MsiUnpublishAssemblies](msiunpublishassemblies-action.md).

## <a name="result"></a>Risultato

ICE83 invia i seguenti errori.



| Errore ICE83                                                                                                   | Descrizione                                                                                                                                                                                                    |
|---------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Il percorso della chiave per l'assembly SxS Win32 (componente \_ = \[ 1 \] ) non deve essere il file manifesto                       | ICE83 Invia questo errore quando il campo del percorso di un assembly Win32 è impostato sul relativo file manifesto (componente. GetPath = = MsiAssembly. file \_ manifest). \[1 \] è il percorso di un percorso della tabella Component                          |
| Entrambe le azioni MsiPublishAssemblies e MsiUnpublishAssemblies devono essere presenti nella tabella InstallExecuteSequence. | ICE83 Invia questo errore quando è presente almeno una voce nella tabella MsiAssembly, ma la tabella InstallExecuteSequence non contiene sia l'azione MsiAssemblyPublish che l'azione MsiAssemblyUnpublish. |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Riferimento ghiaccio](ice-reference.md)
</dt> </dl>

 

 



