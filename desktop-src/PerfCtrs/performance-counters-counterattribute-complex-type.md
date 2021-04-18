---
description: Definisce un attributo di un contatore che specifica la modalità di visualizzazione dei dati del contatore in un'applicazione consumer.
ms.assetid: 3749501b-4f3e-42e5-b1d5-2700b6d4a48a
title: Tipo complesso counterAttribute
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- kbSyntax
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: ee1b34a3a802f0f7c79815956c3a364522ce0962
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106312134"
---
# <a name="counterattribute-complex-type"></a>Tipo complesso counterAttribute

Definisce un attributo di un contatore che specifica la modalità di visualizzazione dei dati del contatore in un'applicazione consumer.

``` syntax
<xs:complexType name="counterAttribute">
    <xs:simpleContent>
        <xs:extension
            base="xs:string"
        >
            <xs:attribute name="name"
                use="required"
            >
                <xs:simpleType>
                    <xs:restriction
                        base="xs:string"
                    >
                        <xs:enumeration
                            value="reference"
                         />
                        <xs:enumeration
                            value="noDisplay"
                         />
                        <xs:enumeration
                            value="noDigitGrouping"
                         />
                        <xs:enumeration
                            value="displayAsHex"
                         />
                        <xs:enumeration
                            value="displayAsReal"
                         />
                    </xs:restriction>
                </xs:simpleType>
            </xs:attribute>
        </xs:extension>
    </xs:simpleContent>
</xs:complexType>
```

## <a name="attributes"></a>Attributi



| Nome | Tipo | Descrizione                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
|------|------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| name |      | Nome dell'attributo di visualizzazione da applicare. È possibile specificare uno dei nomi seguenti:<br/> <dl> <dt><span id="reference"></span><span id="REFERENCE"></span>riferimento</dt> <dd> Recuperare il valore del contatore per riferimento anziché per valore.<br/> </dd> <dt><span id="noDisplay"></span><span id="nodisplay"></span><span id="NODISPLAY"></span>nodisplay</dt> <dd> Non visualizzare il valore del contatore. In genere, si utilizza questo attributo se i dati del contatore vengono utilizzati come input per il calcolo del valore di un altro contatore. <br/> </dd> <dt><span id="noDigitGrouping"></span><span id="nodigitgrouping"></span><span id="NODIGITGROUPING"></span>noDigitGrouping</dt> <dd> Le applicazioni consumer o di monitoraggio non devono usare separatori di cifre durante la visualizzazione dei valori dei contatori. <br/> </dd> <dt><span id="displayAsHex"></span><span id="displayashex"></span><span id="DISPLAYASHEX"></span>displayAsHex</dt> <dd> Le applicazioni consumer o di monitoraggio devono visualizzare il valore del contatore come valore esadecimale anziché come valore intero predefinito.<br/> </dd> <dt><span id="displayAsReal"></span><span id="displayasreal"></span><span id="DISPLAYASREAL"></span>displayAsReal</dt> <dd> Le applicazioni consumer o di monitoraggio devono visualizzare il valore del contatore come numero reale, anziché il valore intero predefinito. <br/> </dd> </dl> |



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>       |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/> |



 

 




