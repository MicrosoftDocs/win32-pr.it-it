---
title: Enumerazioni DirectML
description: Le enumerazioni seguenti sono dichiarate in DirectML.h.
ms.localizationpriority: low
ms.topic: article
ms.date: 11/06/2020
ms.custom: 19H1
ms.openlocfilehash: a74ce2fc3b5bcf94a97d7f51cec20d5f9f0d8e9837a7b59d2f1bdea80328db90
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119953101"
---
# <a name="directml-enumerations"></a>Enumerazioni DirectML

Le enumerazioni seguenti sono dichiarate in DirectML.h.

## <a name="in-this-section"></a>Contenuto della sezione

| Argomento e descrizione |
|-|
| [**DML_AXIS_DIRECTION**](/windows/desktop/api/directml/ne-directml-dml_axis_direction). Definisce costanti che specificano la direzione di un'operazione lungo l'asse specificato per l'operatore (ad esempio, somma, selezione degli elementi in alto a k, selezione dell'elemento minimo). |
| [**DML_BINDING_TYPE**](/windows/desktop/api/directml/ne-directml-dml_binding_type). Definisce costanti che specificano la natura delle risorse a cui fa riferimento una descrizione [dell'associazione DML_BINDING_DESC struttura](/windows/desktop/api/directml/ns-directml-dml_binding_desc). |
| [**DML_CONVOLUTION_DIRECTION**](/windows/desktop/api/directml/ne-directml-dml_convolution_direction). Definisce costanti che specificano una direzione per l'operatore di convoluzione DirectML (come descritto dalla [DML_CONVOLUTION_OPERATOR_DESC struttura](/windows/desktop/api/directml/ns-directml-dml_convolution_operator_desc)). |
| [**DML_CONVOLUTION_MODE**](/windows/desktop/api/directml/ne-directml-dml_convolution_mode). Definisce costanti che specificano una modalità per l'operatore di convoluzione DirectML (come descritto dalla [DML_CONVOLUTION_OPERATOR_DESC struttura](/windows/desktop/api/directml/ns-directml-dml_convolution_operator_desc)). |
| [**DML_CREATE_DEVICE_FLAGS**](/windows/desktop/api/directml/ne-directml-dml_create_device_flags). Fornisce opzioni di creazione del dispositivo aggiuntive a [DMLCreateDevice.](/windows/desktop/api/directml/nf-directml-dmlcreatedevice) |
| [**DML_DEPTH_SPACE_ORDER**](/windows/desktop/api/directml/ne-directml-dml_depth_space_order). Definisce le costanti che controllano la trasformazione applicata negli operatori DirectML DML_OPERATOR_DEPTH_TO_SPACE1 [e](/windows/win32/api/directml/ne-directml-dml_operator_type) **DML_OPERATOR_SPACE_TO_DEPTH1**. |
| [**DML_EXECUTION_FLAGS**](/windows/desktop/api/directml/ne-directml-dml_execution_flags). Fornisce opzioni a DirectML per controllare l'esecuzione degli operatori. |
| [**DML_FEATURE**](/windows/desktop/api/directml/ne-directml-dml_feature). Definisce un set di funzionalità e funzionalità facoltative su cui è possibile eseguire query dal dispositivo DirectML. |
| [**DML_GRAPH_EDGE_TYPE**](/windows/desktop/api/directml/ne-directml-dml_graph_edge_type). Definisce costanti che specificano un tipo di bordo del grafo. Vedere [DML_GRAPH_EDGE_DESC](/windows/win32/api/directml/ns-directml-dml_graph_edge_desc) per l'utilizzo di questa enumerazione. |
| [**DML_GRAPH_NODE_TYPE**](/windows/desktop/api/directml/ne-directml-dml_graph_node_type). Definisce costanti che specificano un tipo di nodo del grafo. Vedere [DML_GRAPH_NODE_DESC](/windows/win32/api/directml/ns-directml-dml_graph_node_desc) per l'utilizzo di questa enumerazione. |
| [**DML_INTERPOLATION_MODE**](/windows/desktop/api/directml/ne-directml-dml_interpolation_mode). Definisce costanti che specificano una modalità per l'operatore DirectML upsample 2-D (come descritto dalla struttura DML_UPSAMPLE_2D_OPERATOR_DESC [).](/windows/desktop/api/directml/ns-directml-dml_upsample_2d_operator_desc) |
| [**DML_MATRIX_TRANSFORM**](/windows/desktop/api/directml/ne-directml-dml_matrix_transform). Definisce costanti che specificano una trasformazione di matrice da applicare a un tensore DirectML. |
| [**DML_OPERATOR_TYPE**](/windows/desktop/api/directml/ne-directml-dml_operator_type). Definisce il tipo di una descrizione dell'operatore. |
| [**DML_PADDING_MODE**](/windows/desktop/api/directml/ne-directml-dml_padding_mode). Definisce costanti che specificano una modalità per l'operatore di riempimento DirectML (come descritto dalla [DML_PADDING_OPERATOR_DESC struttura](/windows/desktop/api/directml/ns-directml-dml_padding_operator_desc)). |
| [**DML_RANDOM_GENERATOR_TYPE**](/windows/win32/api/directml/ne-directml-dml_random_generator_type). Definisce costanti che specificano tipi di generatore di numeri casuali. |
| [**DML_RECURRENT_NETWORK_DIRECTION**](/windows/desktop/api/directml/ne-directml-dml_recurrent_network_direction). Definisce costanti che specificano una direzione per un operatore DirectML ricorrente. |
| [**DML_REDUCE_FUNCTION**](/windows/desktop/api/directml/ne-directml-dml_reduce_function). Definisce le costanti che specificano l'algoritmo di riduzione specifico da usare per l'operatore di riduzione DirectML (come descritto dalla DML_REDUCE_OPERATOR_DESC [struttura](/windows/desktop/api/directml/ns-directml-dml_reduce_operator_desc)). |
| [**DML_TENSOR_DATA_TYPE**](/windows/desktop/api/directml/ne-directml-dml_tensor_data_type). Specifica il tipo di dati dei valori in un tensore. |
| [**DML_TENSOR_FLAGS**](/windows/desktop/api/directml/ne-directml-dml_tensor_flags). Specifica opzioni aggiuntive in una descrizione tensore. |
| [**DML_TENSOR_TYPE**](/windows/desktop/api/directml/ne-directml-dml_tensor_type). Identifica un tipo di descrizione del tensore. |

## <a name="related-topics"></a>Argomenti correlati

* [Informazioni di riferimento su DirectML](direct3d-directml-reference.md)
* [Informazioni di riferimento di base](direct3d-12-core-reference.md)
* [Informazioni di riferimento su Direct3D 12](direct3d-12-reference.md)