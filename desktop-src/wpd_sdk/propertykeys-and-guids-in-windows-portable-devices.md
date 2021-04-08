---
description: PROPERTYKEYs e GUID nei dispositivi portatili Windows
ms.assetid: 3f9e9f29-37dd-47b0-997e-de81966efce2
title: PROPERTYKEYs e GUID nei dispositivi portatili Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c28cbe76b76eda04852cd1afcbb11b85b0a185d1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103883150"
---
# <a name="propertykeys-and-guids-in-windows-portable-devices"></a>PROPERTYKEYs e GUID nei dispositivi portatili Windows

Una proprietà o un comando è identificato da una struttura PROPERTYKEY. Una struttura PROPERTYKEY è costituita da due parti: un GUID (il membro fmtid) e un valore DWORD (il membro PID). La parte GUID viene utilizzata per indicare la categoria a cui appartiene la proprietà o il comando (ovvero, le proprietà correlate appartengono alla stessa categoria e i comandi correlati appartengono alla stessa categoria; pertanto avranno lo stesso fmtid). La parte DWORD indica l'ID della proprietà o del comando e viene utilizzata per distinguere le singole proprietà o comandi all'interno di una proprietà o di una categoria di comandi, ovvero i valori PID per le proprietà o i comandi nella stessa categoria saranno diversi.

La sezione di riferimento di questo documento descrive tutti i valori PROPERTYKEY definiti da WPD; questi valori corrispondono a comandi, proprietà e risorse. Se si crea un valore PROPERTYKEY personalizzato, è necessario definire una nuova categoria **GUID** ; Non riutilizzare i valori **GUID** WPD o rischiare conflitti con PROPERTYKEYs esistenti e futuri specificati da WPD.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Panoramica dell'applicazione**](application-overview.md)
</dt> <dt>

[**Comandi**](commands.md)
</dt> <dt>

[**GUID formato oggetto**](object-format-guids.md)
</dt> <dt>

[**Proprietà e attributi**](properties-and-attributes.md)
</dt> <dt>

[**Requisiti per gli oggetti**](requirements-for-objects.md)
</dt> </dl>

 

 



