---
description: Quando si trasferiscono valori tra l'applicazione host e un parametro Effect, i dati vengono scritti come previsto quando il tipo di dati di origine (nell'applicazione host) corrisponde al tipo di dati di destinazione (nel parametro Effect).
ms.assetid: 4f3ef14a-7d67-45fe-9282-541221815d1f
title: Cast e conversione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 90b8ab6ec3fccd8dc57d503de18ffe1e9e321377
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104126693"
---
# <a name="casting-and-conversion"></a>Cast e conversione

Quando si trasferiscono valori tra l'applicazione host e un parametro Effect, i dati vengono scritti come previsto quando il tipo di dati di origine (nell'applicazione host) corrisponde al tipo di dati di destinazione (nel parametro Effect). Quando i tipi di dati sono diversi, il cast si verifica quando i dati di origine vengono ridisposti per adattarsi alla destinazione.

DXSAS definisce le seguenti regole di conversione del tipo. Si tratta di un superset delle regole di conversione dei tipi Effect (. FX) e HLSL. DXSAS definisce anche alcuni [modificatori di valore di parametro](#parameter-value-modifiers) che possono influire sul valore trasferito dall'applicazione host a un parametro associato.

## <a name="type-casting"></a>Cast di tipo

La tabella seguente elenca il cast che verrà eseguito quando un tipo di dati viene trasferito a un altro tipo di dati:



| Tipo di origine                                  | Tipo destinazione                             | Comportamento                                                                                                                                                                                                                                                                                                                                                                                                 |
|----------------------------------------------|----------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| float                                        | INT                                          | Arrotonda per difetto.                                                                                                                                                                                                                                                                                                                                                                                      |
| float, int                                   | bool                                         | I valori diversi da 0 in base a un confronto non uguale a 0 (int) o 0,0 (float) sono considerati true. in caso contrario, il valore viene considerato false.                                                                                                                                                                                                                                         |
| INT                                          | float                                        |                                                                                                                                                                                                                                                                                                                                                                                                          |
| bool                                         | int, float                                   | False viene convertito in zero. True viene convertito in uno.                                                                                                                                                                                                                                                                                                                                                     |
| texture1D, texture2D, texture3D, textureCUBE | trama                                      | La trama di destinazione viene considerata come il tipo di trama di origine.                                                                                                                                                                                                                                                                                                                                               |
| string                                       | texture1D, texture2D, texture3D, textureCUBE | Il valore stringa viene considerato come un indirizzo di risorsa e risolto in modo analogo all' [annotazione di inizializzazione dei parametri](parameter-initialization-annotation.md). Se non è possibile risolvere l'indirizzo della risorsa, il cast non è valido e le applicazioni host devono restituire un errore. Se la risorsa viene risolta correttamente, il tipo dell'espressione viene considerato come lo stesso tipo della risorsa risolta. |



 

## <a name="class-casting"></a>Cast della classe

Oltre alle regole di cast del tipo descritte in precedenza, DXSAS definisce il set di regole di cast necessarie per la conversione tra i tipi di classe. Le matrici di colonne (N x 1), le matrici di riga (1 x N) e le strutture numeriche vengono considerate come vettori.

I parametri della matrice di effetti e le variabili della matrice HLSL possono definire se il valore è una matrice di righe o colonne principali; Tuttavia, le API DirectX considerano sempre [**D3DMATRIX**](d3dmatrix.md) e [**D3DXMATRIX**](d3dxmatrix.md) come row-major.



| Classe di origine | Classe di destinazione | Comportamento                                                                                                                                                                                                                                                                                                                                        |
|--------------|-------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Scalare       | Scalare            | Applicare il cast del tipo.                                                                                                                                                                                                                                                                                                                             |
| Scalare       | Vettore            | Replicare il valore dell'origine scalare in ogni componente del vettore di destinazione dopo l'applicazione del comportamento di cast e conversione del tipo descritto nel cast dei tipi.                                                                                                                                                                             |
| Scalare       | Matrice            | Replicare il valore dell'origine scalare in ogni componente della matrice di destinazione dopo aver applicato il comportamento di cast e conversione del tipo descritto nel cast del tipo.                                                                                                                                                                             |
| Scalare       | Oggetto            | Cast non valido. Le applicazioni host devono restituire un errore.                                                                                                                                                                                                                                                                                           |
| Scalare       | Struttura         | Valido solo se la struttura di destinazione contiene solo elementi numerici. Se valido, replicare il valore dell'origine scalare in ogni componente della struttura di destinazione dopo aver applicato il comportamento di cast e conversione del tipo descritto nel cast dei tipi.                                                                                        |
| Vettore       | Scalare            | Il valore scalare di destinazione riceve il valore del primo componente del vettore di origine dopo aver applicato il comportamento di cast e conversione del tipo descritto nel [cast del tipo](#type-casting).                                                                                                                                                       |
| Vettore       | Vettore            | Cast non valido se il vettore di destinazione ha più componenti rispetto al vettore di origine. Il vettore di destinazione riceve i valori più a sinistra del vettore di origine dopo aver applicato il comportamento di cast e conversione del tipo descritto nel [cast del tipo](#type-casting). I rimanenti componenti più a destra del vettore di origine vengono persi.             |
| Vettore       | Matrice            | Cast non valido a meno che il vettore di origine non abbia lo stesso numero di componenti della matrice di destinazione. Se il cast è valido, viene applicato il comportamento del cast vettoriale a vettore.                                                                                                                                                             |
| Vettore       | Oggetto            | Cast non valido. Le applicazioni host devono restituire un errore.                                                                                                                                                                                                                                                                                           |
| Vettore       | Struttura         | Valido solo se la struttura di destinazione ha solo elementi numerici e non contiene più elementi del vettore di origine con componenti. Gli elementi della struttura di destinazione ricevono i componenti più a sinistra del vettore di origine dopo aver applicato il comportamento di cast e conversione del tipo descritto nel [cast del tipo](#type-casting).      |
| Matrice       | Scalare            | Il valore scalare di destinazione riceve il valore del valore superiore sinistro della matrice di origine dopo aver applicato il comportamento di cast e conversione del tipo descritto nel [cast del tipo](#type-casting).                                                                                                                                                 |
| Matrice       | Vettore            | Cast non valido a meno che la matrice di origine non abbia lo stesso numero di componenti del vettore di destinazione. Se il cast è valido, viene applicato il comportamento del cast vettore a vettore sopra riportato.                                                                                                                                                       |
| Matrice       | Matrice            | Cast non valido se la matrice di destinazione contiene più componenti rispetto alla matrice di origine. La matrice di destinazione riceve i valori in alto a sinistra della matrice di origine dopo aver applicato il comportamento di cast e conversione del tipo descritto nel [cast del tipo](#type-casting). I rimanenti componenti più in basso a destra della matrice di origine vengono persi. |
| Matrice       | Oggetto            | Cast non valido. Le applicazioni host devono restituire un errore.                                                                                                                                                                                                                                                                                           |
| Matrice       | Struttura         | La dimensione della struttura deve essere uguale alla dimensione della matrice e tutti i componenti della struttura devono essere numerici.                                                                                                                                                                                                                          |
| Oggetto       | Scalare            | Cast non valido. Le applicazioni host devono restituire un errore.                                                                                                                                                                                                                                                                                           |
| Oggetto       | Vettore            | Cast non valido. Le applicazioni host devono restituire un errore.                                                                                                                                                                                                                                                                                           |
| Oggetto       | Matrice            | Cast non valido. Le applicazioni host devono restituire un errore.                                                                                                                                                                                                                                                                                           |
| Oggetto       | Oggetto            | Valido se i tipi degli oggetti sono identici e in base al comportamento definito nel [cast del tipo](#type-casting).                                                                                                                                                                                                                   |
| Struttura    | Scalare            | Valido se la struttura di origine contiene almeno un membro numerico. Il valore scalare di destinazione riceve il valore del primo membro numerico della struttura di origine dopo aver applicato il comportamento di cast e conversione del tipo descritto nel [cast del tipo](#type-casting).                                                                                |
| Struttura    | Vettore            | La struttura di origine deve essere almeno la dimensione del vettore. I primi componenti devono essere numerici fino alla dimensione del vettore di destinazione.                                                                                                                                                                                                    |
| Struttura    | Matrice            | La struttura di origine deve essere almeno la dimensione del vettore. I primi componenti devono essere numerici fino alla dimensione del vettore di destinazione.                                                                                                                                                                                                    |
| Struttura    | Struttura         | La struttura di destinazione non deve essere maggiore della struttura di origine. È necessario che esista un cast valido tra tutti i rispettivi componenti di origine e destinazione.                                                                                                                                                                                       |



 

## <a name="parameter-value-modifiers"></a>Modificatori del valore del parametro

Le annotazioni del modificatore di parametro aggiungono informazioni aggiuntive a un parametro in modo che i dati del parametro possano essere interpretati correttamente. È ad esempio possibile che sia necessario esprimere un vettore con dati normalizzati oppure che una lunghezza può essere misurata in pollici. Le annotazioni del modificatore del valore del parametro esprimono queste informazioni aggiuntive in modo che le applicazioni host possano trasformare i valori correttamente quando i dati vengono trasferiti a un parametro di

Questi sono i modificatori di parametro:



| Annotazioni del modificatore del valore del parametro | Descrizione                                    |
|--------------------------------------|------------------------------------------------|
| [SasNormalize](#sasnormalize)        | Specificare se un vettore è normalizzato o meno. |
| [SasUnits](#sasunits)                | Specificare le unità di misura per un parametro.  |



 

### <a name="sasnormalize"></a>SasNormalize

L'annotazione SasNormalize indica che il parametro associato deve essere un valore normalizzato ogni volta che viene assegnato. Questa annotazione influiscono solo sui parametri float2, float3 e float4.


```
string SasNormalize = "Value";
```



dove value è true o false.

Ecco un esempio:


```
float3 UpNormal
<
  bool SasNormalize = "True";
>;
```



### <a name="sasunits"></a>SasUnits

I dati dei parametri degli effetti sono presenti nelle unità seguenti:


```
string SasUnits = "Value";
```



dove value è uno dei seguenti:



| Tipo di misurazione     | Valore        | Descrizione                    |
|----------------------|--------------|--------------------------------|
| Nessuna unità             | stringa vuota | Nessuna unità                       |
| Distanza             | MM           | Millimetri                    |
|                      | cm           | Centimetri                    |
|                      | m            | Metri                         |
|                      | km           | Chilometri                     |
| Angle                | rad          | Radians                        |
| Tempo                 | ms           | Millisecondi                   |
|                      | sec          | Secondi                        |
|                      | min          | Minuti                        |
|                      | h           | Ore                          |
| Velocità lineare      | mm/sec       | Millimetri al secondo         |
|                      | cm/sec       | Centimetri al secondo         |
|                      | m/sec        | Contatori al secondo              |
|                      | m/hr         | Contatori all'ora                |
|                      | km/ora        | Chilometri all'ora            |
| Accelerazione lineare  | mm/sec ²      | Millimetri al secondo quadrati |
|                      | cm/sec ²      | Centimetri al secondo quadrati |
|                      | m/sec ²       | Metri al secondo quadrati      |
|                      | m/hr ²        | Contatori all'ora quadrati        |
|                      | km/hr ²       | Chilometri per ora quadrati    |
| Velocità angolare     | rad/sec      | Radianti al secondo             |
| Accelerazione angolare | rad/sec ²     | Radianti al secondo quadrati     |
| Area                 | mm ²          | Millimetri quadrati            |
|                      | cm ²          | Centimetri quadrati            |
|                      | mq           | Metri quadrati                 |
|                      | km2          | Chilometri quadrati             |
| Volume               | mm ³          | Millimetri cubid              |
|                      | cm          | Centimetri cubi              |
|                      | M3           | Contatori cubi                   |
|                      | km ³          | Chilometri cubi               |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Informazioni di riferimento sulla semantica e le annotazioni standard DirectX](dx9-graphics-reference-effects-dxsas.md)
</dt> </dl>

 

 



