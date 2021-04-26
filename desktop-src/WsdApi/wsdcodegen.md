---
description: Elemento radice di un file di script XML del generatore di codice WSDAPI.
ms.assetid: 3d40172b-6ba1-4e42-9a1a-519c8e88c2b1
title: elemento wsdCodeGen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9861617854e0e75575f2993717f5b2a86515fb0f
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/26/2021
ms.locfileid: "107994678"
---
# <a name="wsdcodegen-element"></a>elemento wsdCodeGen

Elemento radice di un file script XML del generatore di codice WSDAPI.

## <a name="usage"></a>Utilizzo

``` syntax
<wsdCodeGen
  ConfigFileVersion = "Any character string.">
  child elements
</wsdCodeGen>
```

## <a name="attributes"></a>Attributi



| Attributo                        | Type                             | Obbligatoria       | Descrizione                                                                                  |
|----------------------------------|----------------------------------|----------------|----------------------------------------------------------------------------------------------|
| **ConfigFileVersion**<br/> | Qualsiasi stringa di caratteri.<br/> | Sì<br/> | Versione del file di configurazione. L'unico valore valido è "1.0".<br/> <br/> |



## <a name="child-elements"></a>Elementi figlio



| Elemento                                                         | Descrizione                                                                                                                                                                                                                 |
|-----------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**autoStatic**](autostatic.md)<br/>                     | Indica se WsdCodeGen deve provare a contrassegnare automaticamente determinati campi generati come statici. Questa opzione è abilitata per impostazione predefinita.<br/> <br/>                                                                 |
| [**ﬁle**](file.md)<br/>                                 | Indica al generatore di codice di generare un file.<br/> <br/>                                                                                                                                                       |
| [**hostMetadata**](hostmetadata.md)<br/>                 | Metadati di hosting per il dispositivo da implementazione. Questo elemento viene usato solo per le implementazioni del dispositivo (host).<br/> <br/>                                                                                 |
| [**layerNumber**](layernumber.md)<br/>                   | Numero del livello di codice da generare. I numeri di livello vengono usati nelle tabelle di runtime per distinguere un livello di codice per un altro. WSDAPI usa il codice generato con un numero di livello 0.<br/> <br/> |
| [**layerPrefix**](layerprefix.md)<br/>                   | Prefisso da utilizzare nel codice generato per garantire l'univocità dei simboli generati. WSDAPI usa il prefisso "WSD".<br/> <br/>                                                                                     |
| [**Macro**](macro.md)<br/>                               | Definisce il testo o CDATA che deve essere riutilizzato [**dall'elemento include.**](include.md)<br/> <br/>                                                                                                                        |
| [**Namespace**](namespace.md)<br/>                       | Descrive uno spazio dei nomi da utilizzare per la generazione del codice.<br/> <br/>                                                                                                                                                |
| [**relationshipMetadata**](relationshipmetadata.md)<br/> | Descrive l'host e i metadati ospitati per il dispositivo.<br/> <br/>                                                                                                                                               |
| [**thisModelMetadata**](thismodelmetadata.md)<br/>       | Metadati del produttore e del modello per il dispositivo da implementazione. Questo elemento viene usato solo per le implementazioni del dispositivo (host).<br/> <br/>                                                                  |
| [**Wsdl**](wsdl.md)<br/>                                 | Specifica un file WSDL da elaborare per le informazioni sul contratto.<br/> <br/>                                                                                                                                           |
| [**Xsd**](xsd.md)<br/>                                   | Specifica un file XSD da elaborare per le informazioni sul contratto.<br/> <br/>                                                                                                                                           |



### <a name="child-element-sequence"></a>Sequenza di elementi figlio

``` syntax
(
  layerNumber?, 
  layerPrefix?, 
  autoStatic?, 
  hostMetadata?, 
  thisModelMetadata?, 
  nameSpace*, 
  wsdl*, 
  xsd*, 
  file*, 
  macro*, 
  relationshipMetadata*
)
```

## <a name="parent-elements"></a>Elementi padre

Non ci sono elementi padre.

## <a name="remarks"></a>Commenti

In generale, [**gli elementi di file**](file.md) devono verificarsi per ultimi perché generano codice che usa i dati specificati dagli altri elementi.

## <a name="element-information"></a>Informazioni sull'elemento



| Label | Valore |
|-------------------------------------|---------------|
| Sistema minimo supportato<br/> | Windows Vista |
| Può essere vuoto                        | Sì           |



 

 




