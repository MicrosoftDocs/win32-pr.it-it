---
description: ICE41 verifica che le voci della classe e le tabelle di estensioni facciano riferimento alle voci della tabella dei componenti che implementano l'oggetto o l'estensione della classe del componente.
ms.assetid: 43572322-ba23-4f99-be34-e572d4c6e3eb
title: ICE41
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a4bc6c0a8bb634706750810484963e56b6d6e0ec
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106314216"
---
# <a name="ice41"></a>ICE41

ICE41 verifica che le voci della [classe](class-table.md) e le tabelle di [estensioni](extension-table.md) facciano riferimento alle voci della [tabella dei componenti](component-table.md) che implementano l'oggetto o l'estensione della classe del componente.

## <a name="result"></a>Risultato

ICE41 Invia un errore se esiste una funzionalità che non contiene il componente che implementa l'estensione o l'oggetto della classe.

## <a name="example"></a>Esempio

ICE41 segnala gli errori seguenti per l'esempio illustrato.



| Errore ICE41                                                                                                                                                                                    | Descrizione                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| La classe {00000000-0000-0000-0000-0000000000000} fa riferimento alla funzionalità Funzionalità2 e al componente Component1, ma il componente non è associato a tale funzionalità nella tabella FeatureComponents. | Esiste una funzionalità che non contiene il componente che implementa l'oggetto classe. Ciò significa che il programma di installazione non installa il componente con la funzionalità e che la pubblicità potrebbe non funzionare come previsto. Per correggere l'errore, modificare la voce nella colonna funzionalità \_ della voce [tabella classi](class-table.md) per fare riferimento a una funzionalità che installa il componente elencato nella \_ colonna componente o modificare la funzionalità e il componente associati nella [tabella FeatureComponents](featurecomponents-table.md).<br/>          |
| Extension. Feature1 fa riferimento a feature Component2 e Component, ma il componente non è associato a tale funzionalità nella tabella FeatureComponents.                                | Esiste una funzionalità che non contiene il componente che implementa l'estensione. Ciò significa che il programma di installazione non installa il componente con la funzionalità e che la pubblicità potrebbe non funzionare come previsto. Per correggere l'errore, modificare la voce nella colonna funzionalità \_ della voce della [tabella di estensione](extension-table.md) in modo che faccia riferimento a una funzionalità che installa il componente elencato nella \_ colonna componente o modificare la funzionalità e il componente associati nella [tabella FeatureComponents](featurecomponents-table.md).<br/> |



 

[Tabella FeatureComponents](featurecomponents-table.md) (parziale)



| Funzionalità\_ |
|-----------|
| Feature1  |
| Funzionalità2  |



 

[Tabella classi](class-table.md) (parziale)



| CLSID                                  | Componente\_ | Funzionalità\_ |
|----------------------------------------|-------------|-----------|
| {00000000-0000-0000-0000-000000000000} | Component1  | Funzionalità2  |



 

[Tabella classi](class-table.md) (parziale)



| Estensione | Componente\_ | Funzionalità\_ |
|-----------|-------------|-----------|
| .      | Component2  | Feature1  |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Riferimento ghiaccio](ice-reference.md)
</dt> </dl>

 

 




