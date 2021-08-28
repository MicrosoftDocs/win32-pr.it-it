---
description: ICE41 verifica che le voci nelle tabelle Class ed Extension facciano riferimento alle voci nella tabella Component che implementano l'oggetto classe o l'estensione del componente.
ms.assetid: 43572322-ba23-4f99-be34-e572d4c6e3eb
title: ICE41
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0c220e43cf8a275e520f5babe1ca609a1cee2194b4c08f8dcdafabe6d73bdca4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119581111"
---
# <a name="ice41"></a>ICE41

ICE41 verifica che le voci nelle tabelle [Class](class-table.md) ed [Extension](extension-table.md) facciano riferimento alle voci nella tabella [Component](component-table.md) che implementano l'oggetto classe o l'estensione del componente.

## <a name="result"></a>Risultato

ICE41 invia un errore se è presente una funzionalità che non contiene il componente che implementa l'oggetto o l'estensione della classe.

## <a name="example"></a>Esempio

ICE41 segnala gli errori seguenti per l'esempio illustrato.



| Errore ICE41                                                                                                                                                                                    | Descrizione                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| La classe fa riferimento alla funzionalità Feature2 e al componente Component1, ma tale componente non è associato a {00000000-0000-0000-0000-0000000000000} tale funzionalità nella tabella FeatureComponents. | Esiste una funzionalità che non contiene il componente che implementa l'oggetto classe. Ciò significa che il programma di installazione non installa il componente con la funzionalità e che la pubblicità potrebbe non funzionare come previsto. Per correggere l'errore, modificare la voce nella colonna Funzionalità della voce di tabella Classe per fare riferimento a una funzionalità che installa il componente elencato nella colonna Componente o modificare la funzionalità e il componente associati nella \_ [](class-table.md) \_ tabella [FeatureComponents](featurecomponents-table.md).<br/>          |
| L'estensione .yip fa riferimento alla funzionalità Feature1 e al componente Component2, ma tale componente non è associato a tale funzionalità nella tabella FeatureComponents.                                | Esiste una funzionalità che non contiene il componente che implementa l'estensione. Ciò significa che il programma di installazione non installa il componente con la funzionalità e che la pubblicità potrebbe non funzionare come previsto. Per correggere l'errore, modificare la voce nella colonna Funzionalità della voce della tabella Estensione in modo da fare riferimento a una funzionalità che installa il componente elencato nella colonna Componente o modificare la funzionalità e il componente associati nella \_ [](extension-table.md) \_ tabella [FeatureComponents](featurecomponents-table.md).<br/> |



 

[Tabella FeatureComponents](featurecomponents-table.md) (parziale)



| Funzionalità\_ |
|-----------|
| Funzionalità1  |
| Funzionalità 2  |



 

[Tabella di classi](class-table.md) (parziale)



| CLSID                                  | Componente\_ | Funzionalità\_ |
|----------------------------------------|-------------|-----------|
| {00000000-0000-0000-0000-000000000000} | Componente1  | Funzionalità 2  |



 

[Tabella di classi](class-table.md) (parziale)



| Estensione | Componente\_ | Funzionalità\_ |
|-----------|-------------|-----------|
| .yip      | Componente2  | Funzionalità1  |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Informazioni di riferimento su ICE](ice-reference.md)
</dt> </dl>

 

 




