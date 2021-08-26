---
description: PROPERTYKEYs e GUID in Windows dispositivi portatili
ms.assetid: 3f9e9f29-37dd-47b0-997e-de81966efce2
title: PROPERTYKEYs e GUID in Windows dispositivi portatili
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 80100b043383074f58bc27fe8e9782c4fd6d2e4f3841a28f37035f39d23cc7c5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120054871"
---
# <a name="propertykeys-and-guids-in-windows-portable-devices"></a>PROPERTYKEYs e GUID in Windows dispositivi portatili

Una proprietà o un comando è identificato da una struttura PROPERTYKEY. Una struttura PROPERTYKEY è costituito da due parti: un GUID (il membro fmtid) e un valore DWORD (membro pid). La parte GUID viene usata per indicare la categoria a cui appartiene la proprietà o il comando, ovvero le proprietà correlate appartengono alla stessa categoria e i comandi correlati appartengono alla stessa categoria, pertanto avranno lo stesso fmtid. La parte DWORD indica l'ID della proprietà o del comando e viene usata per distinguere le singole proprietà o i singoli comandi all'interno di una proprietà o di una categoria di comandi ( ovvero, i valori pid per le proprietà o i comandi nella stessa categoria saranno diversi).

La sezione di riferimento di questo documento descrive tutti i valori PROPERTYKEY definiti da WPD; Questi valori corrispondono a comandi, proprietà e risorse. Se si crea un valore PROPERTYKEY personalizzato, è necessario definire una nuova **categoria GUID.** non riutilizzare i valori **GUID** WPD o si rischia di essere in conflitto con propertyKEY esistenti e futuri specificati da WPD.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Panoramica dell'applicazione**](application-overview.md)
</dt> <dt>

[**Comandi**](commands.md)
</dt> <dt>

[**GUID di formato oggetto**](object-format-guids.md)
</dt> <dt>

[**Proprietà e attributi**](properties-and-attributes.md)
</dt> <dt>

[**Requisiti per gli oggetti**](requirements-for-objects.md)
</dt> </dl>

 

 



