---
description: ICE83 convalida la tabella MsiAssembly.
ms.assetid: dd290c73-6528-482d-8276-ac56d0fec181
title: ICE83
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 78e8014f8feee76e4d1910fb601e186bec928a0fd6d6d34469ce2c2b201b724d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119580751"
---
# <a name="ice83"></a>ICE83

ICE83 convalida la [tabella MsiAssembly](msiassembly-table.md). Questa azione personalizzata ICE invia un errore se il percorso della chiave per un componente contenente un assembly Win32 è impostato sul file manifesto. L'errore viene inserito in modo esplicito se il valore immesso nel campo KeyPath della tabella [Component](component-table.md) è uguale al valore immesso nel campo Manifesto file \_ della tabella MsiAssembly. Questa azione personalizzata ICE invia un errore se è presente almeno un record nella tabella MsiAssembly e la tabella [InstallExecuteSequence](installexecutesequence-table.md) non contiene sia l'azione [MsiPublishAssemblies](msipublishassemblies-action.md) che l'azione [MsiUnpublishAssemblies](msiunpublishassemblies-action.md).

## <a name="result"></a>Risultato

ICE83 pubblica gli errori seguenti.



| Errore ICE83                                                                                                   | Descrizione                                                                                                                                                                                                    |
|---------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Il percorso della chiave per l'assembly SXS Win32 (componente \_ = \[ \] 1) NON DEVE essere il file manifesto                       | ICE83 pubblica questo errore quando il campo KeyPath per un assembly Win32 è impostato sul relativo file manifesto (Component.KeyPath == MsiAssembly.File \_ Manifest). \[1 \] è KeyPath nella tabella Component                          |
| Entrambe le azioni MsiPublishAssemblies e MsiUnpublishAssemblies DEVONO essere presenti nella tabella InstallExecuteSequence. | ICE83 registra questo errore quando è presente almeno una voce nella tabella MsiAssembly, ma la tabella InstallExecuteSequence non contiene sia l'azione MsiAssemblyPublish che l'azione MsiAssemblyUnpublish. |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Informazioni di riferimento su ICE](ice-reference.md)
</dt> </dl>

 

 



